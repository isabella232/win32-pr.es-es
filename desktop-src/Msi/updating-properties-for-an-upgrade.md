---
description: Dado que la actualización cambia el nombre del archivo .msi y cambia el código de componente de algunos componentes, el código de producto de la actualización debe cambiarse del del producto original.
ms.assetid: ebb1a217-fce6-43f0-9139-c0f4422c8fc4
title: Actualizar las propiedades de una actualización
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 750c30a75650ff4009dda799b0542f41f535481f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127254151"
---
# <a name="updating-properties-for-an-upgrade"></a>Actualizar las propiedades de una actualización

Dado que la actualización cambia el nombre del archivo .msi y cambia el código de componente de algunos componentes, el código de producto de la actualización debe cambiarse del del producto original. Para obtener una descripción de los casos en los que se requiere una actualización para cambiar la [**propiedad ProductCode,**](productcode.md) vea [Cambiar el código de producto](changing-the-product-code.md). Una actualización que cambia ProductCode se conoce como actualización [principal.](major-upgrades.md)

La propiedad [**ProductName**](productname.md) del paquete de actualización, la propiedad [**ProductVersion,**](productversion.md) la propiedad [**ProductLanguage**](productlanguage.md) y la propiedad [**UpgradeCode**](upgradecode.md) pueden cambiarse o no modificarse desde el producto original. En función de los valores de estas propiedades, Windows instalador puede determinar si se deben aplicar paquetes de actualización futuros a la actualización actual.

La propiedad especificada en la columna ActionProperty de la [tabla Upgrade](upgrade-table.md) debe agregarse a la [**propiedad SecureCustomProperties.**](securecustomproperties.md)

Use el editor de base de datos para MNP2001.msi y escriba los datos siguientes en la [tabla Property](property-table.md). La lista proporciona vínculos a los temas de referencia para las propiedades del instalador integradas. Los nombres de propiedad que no son vínculos son propiedades definidas por el autor. Muchas de las propiedades se importaron Uisample.msi que se incluye con el SDK. Para obtener más información, [vea Importing the Interfaz de usuario](importing-the-user-interface.md).

[Tabla de propiedades](property-table.md)



| Propiedad                                         | Value                                     |
|--------------------------------------------------|-------------------------------------------|
| [**ARPHELPLINK**](arphelplink.md)               | https://www.microsoft.com/management       |
| BannerBitmap                                     | bannrbmp                                  |
| ButtonText \_ Back                                 | < &back                                |
| ButtonText \_ Browse                               | Br&owse                                   |
| ButtonText \_ Cancel                               | Cancelar                                    |
| ButtonText \_ Exit                                 | &salir                                     |
| ButtonText \_ Finish                               | &finalizar                                   |
| ButtonText \_ Ignore                               | &omitir                                   |
| ButtonText \_ Install                              | &instalación                                  |
| ButtonText \_ Next                                 | &Siguiente >                                |
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
| [**ProductCode**](productcode.md)               | {34CF587C-1D8F-4DD5-ADFE-440F4B593987}    |
| [**Productid**](productid.md)                   | ninguno                                      |
| [**ProductLanguage**](productlanguage.md)       | 3082                                      |
| [**ProductName**](productname.md)               | MNP2001                                   |
| [**ProductVersion**](productversion.md)         | 01.50.0000                                |
| Progreso1                                        | Instalación                                |
| Progreso2                                        | installs                                  |
| [**PROMPTROLLBACKCOST**](promptrollbackcost.md) | P                                         |
| RemoveIcon                                       | removico                                  |
| RepairIcon                                       | repairic                                  |
| Configuración                                            | Configuración                                     |
| True                                             | 1                                         |
| [**UpgradeCode**](upgradecode.md)               | {908E378A-9551-4772-BF1D-5CFAF6FD9CB4}    |
| Asistente                                           | Asistente para la instalación                              |
| SecureCustomProperties                           | OLDAPPFOUND                               |



 

[Continuar](updating-sequence-tables-for-an-upgrade.md)

 

 



