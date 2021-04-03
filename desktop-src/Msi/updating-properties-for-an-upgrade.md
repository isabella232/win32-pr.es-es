---
description: Dado que la actualización cambia el nombre del archivo. msi y cambia el código de componente de algunos componentes, el código de producto de la actualización debe cambiarse del producto original.
ms.assetid: ebb1a217-fce6-43f0-9139-c0f4422c8fc4
title: Actualizar las propiedades de una actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750c30a75650ff4009dda799b0542f41f535481f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104083349"
---
# <a name="updating-properties-for-an-upgrade"></a>Actualizar las propiedades de una actualización

Dado que la actualización cambia el nombre del archivo. msi y cambia el código de componente de algunos componentes, el código de producto de la actualización debe cambiarse del producto original. Para obtener una descripción de los casos en los que se requiere una actualización para cambiar la propiedad [**ProductCode**](productcode.md) , consulte [cambiar el código de producto](changing-the-product-code.md). Una actualización que cambia el ProductCode se conoce como una [actualización principal](major-upgrades.md).

Se puede cambiar la propiedad [**ProductName**](productname.md) del paquete de actualización, la propiedad [**ProductVersion**](productversion.md) , la propiedad [**ProductLanguage**](productlanguage.md) y la propiedad [**UpgradeCode**](upgradecode.md) , o bien no cambiar, del producto original. En función de los valores de estas propiedades, Windows Installer puede determinar si se deben aplicar paquetes de actualización futuros a la actualización actual.

La propiedad especificada en la columna ActionProperty de la [tabla de actualización](upgrade-table.md) debe agregarse a la propiedad [**SecureCustomProperties**](securecustomproperties.md) .

Utilice el editor de base de datos para abrir MNP2001.msi y escriba los datos siguientes en la [tabla de propiedades](property-table.md). La lista proporciona vínculos a los temas de referencia de las propiedades integradas del instalador. Los nombres de propiedad que no son vínculos son propiedades definidas por el autor. Muchas de las propiedades se importaron desde Uisample.msi que vienen con el SDK. Para obtener más información, consulte [importación de la interfaz de usuario](importing-the-user-interface.md).

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
| [**ProductCode**](productcode.md)               | {34CF587C-1D8F-4DD5-ADFE-440F4B593987}    |
| [**IdProducto**](productid.md)                   | ninguno                                      |
| [**ProductLanguage**](productlanguage.md)       | 3082                                      |
| [**ProductName**](productname.md)               | MNP2001                                   |
| [**ProductVersion**](productversion.md)         | 01.50.0000                                |
| Progress1                                        | Instalando                                |
| Progress2                                        | installs                                  |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md) | P                                         |
| RemoveIcon                                       | removico                                  |
| RepairIcon                                       | reparación                                  |
| Configurar                                            | Configurar                                     |
| True                                             | 1                                         |
| [**UpgradeCode**](upgradecode.md)               | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4}    |
| Asistente                                           | Asistente para la instalación                              |
| SecureCustomProperties                           | OLDAPPFOUND                               |



 

[Continuar](updating-sequence-tables-for-an-upgrade.md)

 

 



