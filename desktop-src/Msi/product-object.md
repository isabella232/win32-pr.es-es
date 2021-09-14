---
description: El objeto Product representa una instancia única de un producto anunciado, instalado o desconocido. Se puede crear una instancia del objeto con la propiedad Product como &\# 0034; WindowsInstaller.Installer.Product(ProductCode, UserSid, Context)&\# 0034;.
ms.assetid: 1fa89239-051a-4b3a-913a-12c7c093f35b
title: Objeto Product
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Product
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: f8e9071f26da944c2c5ea206b2f70582d731ef59
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074326"
---
# <a name="product-object"></a>Objeto Product

El **objeto Product** representa una instancia única de un producto anunciado, instalado o desconocido.

Se puede crear una instancia del objeto con la propiedad **Product** como "WindowsInstaller.Installer.Product(*ProductCode*, *UserSid*, *Context*)". *UserSid* debe ser NULL para el contexto por equipo. *UserSid* puede ser NULL para el usuario actual especificado, cuando el contexto no es por equipo. *Se requieren los* *parámetros* ProductCode y Context.

## <a name="members"></a>Members

El **objeto Product** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto Product** tiene estos métodos.



| Método                                                                 | Descripción                                                                                                        |
|:-----------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------|
| [**SourceListAddMediaDisk**](product-sourcelistaddmediadisk.md)       | Agregue un disco al conjunto de discos registrados.<br/>                                                              |
| [**SourceListAddSource**](product-sourcelistaddsource.md)             | Agregue un origen de red o dirección URL a la lista de origen.<br/>                                                         |
| [**SourceListClearAll**](product-sourcelistclearall.md)               | Borra la lista de origen completa del tipo de orígenes especificado.<br/>                                       |
| [**SourceListClearMediaDisk**](product-sourcelistclearmediadisk.md)   | Quite un disco del conjunto de discos registrados de la lista de origen.<br/>                                    |
| [**SourceListClearSource**](product-sourcelistclearsource.md)         | Quite un origen de red o dirección URL de la lista de origen.<br/>                                                    |
| [**SourceListForceResolution**](product-sourcelistforceresolution.md) | Borra el último origen usado. Esto fuerza una resolución de lista de origen la próxima vez que se requiera el origen.<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto Product** tiene estas propiedades.



| Propiedad.                                                      | Descripción                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**ComponentState**](product-componentstate.md)<br/>   | Estado de un componente especificado para esta instancia de producto. <br/>                   |
| [**Contexto**](product-context.md)<br/>                 | Contexto de esta instancia de producto como un valor MSIINSTALLCONTEXT. <br/>                 |
| [**FeatureState**](product-featurestate.md)<br/>       | Estado de una característica especificada para esta instancia de producto. <br/>                     |
| [**InstallProperty**](product-installproperty.md)<br/> | Valor de una propiedad especificada. <br/>                                              |
| [**MediaDisks**](product-mediadisks.md)<br/>           | Enumera todos los discos multimedia de esta instancia de producto.<br/>                        |
| [**ProductCode**](product-productcode.md)<br/>         | Devuelve el código del producto. <br/>                                                       |
| [**SourceListInfo**](product-sourcelistinfo.md)<br/>   | Obtiene y establece las propiedades de la información de origen. Se trata de una propiedad de lectura o escritura.<br/> |
| [**Fuentes**](product-sources.md)<br/>                 | Enumera todos los orígenes de esta instancia de producto.<br/>                            |
| [**Estado**](product-state.md)<br/>                     | Estado de instalación del producto.<br/>                                               |
| [**UserSid**](product-usersid.md)<br/>                 | Devuelve el SID de usuario, con la cuenta en la que está disponible esta instancia del producto.<br/>    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct se define como \_ 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




