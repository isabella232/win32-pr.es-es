---
description: Windows Installer propiedades son variables globales que el instalador usa durante la instalación.
ms.assetid: 1c59939b-de0f-4bf4-ab1f-4f1aa2488bfa
title: Especificar propiedades
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9cd4294f35595e723491398172dc4c73337a1416
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652569"
---
# <a name="specifying-properties"></a>Especificar propiedades

Windows Installer propiedades son variables globales que el instalador usa durante la instalación. Vea las secciones en [propiedades](properties.md). Si en la sección [importar una base de datos en blanco](importing-a-blank-database.md) usada uisample.msi del SDK de Windows Installer, la [tabla de propiedades](property-table.md) de la copia de MNP2000.msi ya contiene muchas propiedades utilizadas por la interfaz de usuario. En esta sección, agregará información adicional a la tabla de propiedades específica de la instalación del ejemplo del Bloc de notas. Vea también el [Grupo tablas de información del programa](program-information-tables-group.md).

Hay cinco propiedades que se requieren en cada paquete de instalación y se deben actualizar para el ejemplo del Bloc de notas en la [tabla de propiedades](property-table.md) de MNP2000.msi:

-   [**ProductCode**](productcode.md)
-   [**ProductLanguage**](productlanguage.md)
-   [**Le**](manufacturer.md)
-   [**ProductVersion**](productversion.md)
-   [**ProductName**](productname.md)

Aunque no es necesario para todos los paquetes de instalación, las aplicaciones que pueden recibir una actualización en el futuro también deben tener una propiedad [**UpgradeCode**](upgradecode.md) . Consulte [preparación de una aplicación para futuras actualizaciones importantes](preparing-an-application-for-future-major-upgrades.md).

Utilice el editor de base de datos para abrir MNP2000.msi y escriba los datos siguientes en la tabla de propiedades. La lista proporciona vínculos a los temas de referencia de las propiedades integradas del instalador. Los nombres de propiedad que no son vínculos son propiedades definidas por el autor. Muchas de las propiedades importadas desde uisample.msi son para la interfaz de usuario de ejemplo. En la sección de la interfaz de usuario más adelante del ejemplo de instalación se describe la interfaz de usuario.

[Tabla de propiedades](property-table.md)



| Propiedad                                         | Value                                     |
|--------------------------------------------------|-------------------------------------------|
| [**ARPHELPLINK**](arphelplink.md)               | https://www.microsoft.com/management       |
| BannerBitmap                                     | bannrbmp                                  |
| \_Volver atrás                                 | < &atrás                                |
| Examinar de ButtonText \_                               | Br&owse                                   |
| ButtonText \_ cancelar                               | Cancelar                                    |
| Salida de ButtonText \_                                 | &salir                                     |
| Fin de ButtonText \_                               | &finalizar                                   |
| ButtonText- \_ omitir                               | &omitir                                   |
| \_Instalar ButtonText                              | &instalar                                  |
| ButtonText \_ siguiente                                 | &siguiente >                                |
| ButtonText \_ no                                   | &no                                       |
| ButtonText \_ Aceptar                                   | Aceptar                                        |
| ButtonText \_ quitar                               | &quitar                                   |
| Restablecer el ButtonText \_                                | &restablecer                                    |
| Resume del ButtonText \_                               | &reanudar                                   |
| Reintento de ButtonText \_                                | &reintentar                                    |
| Valor de ButtonText \_                               | &devolver                                   |
| ButtonText \_ sí                                  | &sí                                      |
| CompleteSetupIcon                                | completar                                  |
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
| [**Le**](manufacturer.md)             | Microsoft                                 |
| [**PIDTemplate**](pidtemplate.md)               | 12345<\#\#\#-%%%%%%%>@@@@@          |
| [**ProductCode**](productcode.md)               | {18A9233C-0B34-4127-A966-C257386270BC}    |
| [**IdProducto**](productid.md)                   | ninguno                                      |
| [**ProductLanguage**](productlanguage.md)       | 3082                                      |
| [**ProductName**](productname.md)               | MNP2000                                   |
| [**ProductVersion**](productversion.md)         | 01.40.0000                                |
| Progress1                                        | Instalando                                |
| Progress2                                        | installs                                  |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md) | P                                         |
| RemoveIcon                                       | removico                                  |
| RepairIcon                                       | reparación                                  |
| Configurar                                            | Configurar                                     |
| True                                             | 1                                         |
| [**UpgradeCode**](upgradecode.md)               | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4}    |
| Asistente                                           | Asistente para la instalación                              |



 

[Continuar](importing-the-installexecutesequence.md)

 

 



