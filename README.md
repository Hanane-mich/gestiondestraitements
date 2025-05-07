# gestiondestraitements
package gestiondestraitements.Model;

import javafx.application.Application;
import javafx.fxml.FXMLLoader;
import javafx.scene.Scene;
import javafx.scene.image.Image;
import javafx.scene.layout.AnchorPane;
import javafx.scene.layout.StackPane;
import javafx.scene.layout.VBox;
import javafx.stage.Stage;

public class GestionDesTraitements extends Application {

    @Override
    public void start(Stage stage) throws Exception {
        // Connexion à la base de données

        // Chargement du fichier FXML pour l'interface graphique
        FXMLLoader loader = new FXMLLoader(getClass().getResource("/gestiondestraitements/View/view.fxml"));
        StackPane root = loader.load(); // Charger la racine FXML
        Scene scene = new Scene(root, 600, 400);
        stage.setScene(scene);
        stage.setTitle("SuiTrait");
        Image img = new Image("Logo.png");
        String css = this.getClass().getResource("/gestiondestraitements/View/Style.css").toExternalForm();
        scene.getStylesheets().add(css);
        stage.getIcons().add(img);
        stage.show();
    }

    public static void main(String[] args) {
        launch(args);
    }
}
