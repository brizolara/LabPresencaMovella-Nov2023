# Aplicacao para acao conjunta Lab Presenca / Movella

Projeto Unity3D da acao conjunta da LabPresenca com a Movella Inc - Novembro 2023.

## Ambiente de desenvolvimento testado:
- Windows 10
- Unity 2021.3.25f1
- Unity Package MVN Live Animation 2023.0.0

## Observações (C#):

Precisei adaptar o código para alguns erros de nível de escopo e de proteção
Em XsensClient.cs, adicionei os namespaces xsens:
```
xsens.XsDataPacket dataPacket = new xsens.XsQuaternionPacket(data);
xsens.XsMvnPose pose = dataPacket.getPose();
```
E nas 3 seguintes classes adicionei public:
```
public class XsQuaternionPacket : XsDataPacket
public abstract class XsDataPacket
public class XsMvnPose
```

## Versão Inicial

* Foi carregada a cena de exemplo da unitypackage da Movella
* Animação FBX de Gangnam Style (baixada de https://www.movella.com/resources/news/motion-capture-files-for-psy-gangnam-style) foi adicionada ao personagem (MvnPuppet), seguindo o tutorial https://movella.my.site.com/XsensKnowledgebase/s/article/FBX-import-into-Unity?language=en_US

## Sobre modelagem e rigging

Utilizar o MvnPuppet como referência
