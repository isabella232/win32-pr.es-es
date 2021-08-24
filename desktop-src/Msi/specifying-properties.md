---
description: Windows Las propiedades del instalador son variables globales que el instalador usa durante una instalación.
ms.assetid: 1c59939b-de0f-4bf4-ab1f-4f1aa2488bfa
title: Especificar propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f538bb354ef793a54f3eb60ddfe7b75b2aa96310abdd8a7331813d887433816
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119627805"
---
# <a name="specifying-properties"></a>Especificar propiedades

Windows Las propiedades del instalador son variables globales que el instalador usa durante una instalación. Vea las secciones de [Propiedades.](properties.md) Si en la sección [Importing a Blank Database](importing-a-blank-database.md) (Importar una base [](property-table.md) de datos en blanco) usó uisample.msi desde el SDK del instalador de Windows, la tabla Property de la copia de MNP2000.msi ya contiene muchas propiedades que usa la interfaz de usuario. En esta sección agregará información adicional a la tabla Property específica de la instalación del Bloc de notas ejemplo. Vea también el grupo [Tablas de información del programa](program-information-tables-group.md).

Hay cinco propiedades que son necesarias en cada paquete de instalación y deben actualizarse para el ejemplo Bloc de notas en la [tabla Property](property-table.md) de MNP2000.msi:

-   [**ProductCode**](productcode.md)
-   [**ProductLanguage**](productlanguage.md)
-   [**Fabricante**](manufacturer.md)
-   [**ProductVersion**](productversion.md)
-   [**Productname**](productname.md)

Aunque no es necesario para todos los paquetes de instalación, las aplicaciones que pueden recibir una actualización en el futuro también deben tener una [**propiedad UpgradeCode.**](upgradecode.md) Consulte [Preparar una aplicación para futuras actualizaciones principales.](preparing-an-application-for-future-major-upgrades.md)

Use el editor de bases de datos para MNP2000.msi y escriba los datos siguientes en la tabla Property. La lista proporciona vínculos a los temas de referencia de las propiedades del instalador integradas. Los nombres de propiedad que no son vínculos son propiedades definidas por el autor. Muchas de las propiedades importadas de uisample.msi son para la interfaz de usuario de ejemplo. En la sección posterior Interfaz de usuario del ejemplo de instalación se describe la interfaz de usuario.

[Tabla de propiedades](property-table.md)



| Propiedad                                         | Value                                     |
|--------------------------------------------------|-------------------------------------------|
| [**ARPHELPLINK**](arphelplink.md)               | https://www.microsoft.com/management       |
| BannerBitmap                                     | bannrbmp                                  |
| ButtonText \_ Back                                 | < &atrás                                |
| ButtonText \_ Browse                               | Br&owse                                   |
| ButtonText \_ Cancel                               | Cancelar                                    |
| ButtonText \_ Exit                                 | &salir                                     |
| ButtonText \_ Finish                               | &finalizar                                   |
| ButtonText \_ Ignore                               | &omitir                                   |
| ButtonText \_ Install                              | &instalación                                  |
| ButtonText \_ Next                                 | &siguiente >                                |
| ButtonText \_ No                                   | &No                                       |
| ButtonText \_ (Aceptar)                                   | Aceptar                                        |
| ButtonText \_ Remove                               | &quitar                                   |
| ButtonText \_ Reset                                | &restablecimiento                                    |
| ButtonText \_ Resume                               | &reanudar                                   |
| ButtonText \_ Retry                                | &reintento                                    |
| ButtonText \_ Return                               | &return                                   |
| ButtonText \_ Sí                                  | &Sí                                      |
| CompleteSetupIcon                                | completi                                  |
| ComponentDownload                                | ftp://anonymous@microsoft.com/components/ |
| CustomSetupIcon                                  | custicon                                  |
| [**DefaultUIFont**](defaultuifont.md)           | DlgFont8                                  |
| DialogBitmap                                     | dlgbmp                                    |
| DlgTitleFont                                     | {&DlgFontBold8}                           |
| ErrorDialog                                      | ErrorDlg                                  |
| ExclamationIcon                                  | exclamic                                  |
| False                                            | 0                                         |
| Iagree                                           | No                                        |
| InfoIcon                                         | info                                      |
| InstallerIcon                                    | insticon                                  |
| [**INSTALLLEVEL**](installlevel.md)             | 3                                         |
| InstallMode                                      | Habitual                                   |
| [**Fabricante**](manufacturer.md)             | Microsoft                                 |
| [**PIDTemplate**](pidtemplate.md)               | 12345<\#\#\#-%%%%%%%>@@@@@          |
| [**ProductCode**](productcode.md)               | {18A9233C-0B34-4127-A966-C257386270BC}    |
| [**Productid**](productid.md)                   | ninguno                                      |
| [**ProductLanguage**](productlanguage.md)       | 3082                                      |
| [**Productname**](productname.md)               | MNP2000                                   |
| [**ProductVersion**](productversion.md)         | 01.40.0000                                |
| Progreso1                                        | Instalación                                |
| Progreso2                                        | installs                                  |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md) | P                                         |
| RemoveIcon                                       | removico                                  |
| RepairIcon                                       | repairic                                  |
| Configuración                                            | Configuración                                     |
| True                                             | 1                                         |
| [**UpgradeCode**](upgradecode.md)               | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4}    |
| Asistente                                           | Asistente para la instalación                              |



 

[Continuar](importing-the-installexecutesequence.md)

 

 



