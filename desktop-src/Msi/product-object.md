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
ms.openlocfilehash: ff05a2f89244da09caa6cd3b26fc4b5d9cdbec95c0fcc3098fddf0c39dc68519
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118627678"
---
# <a name="product-object"></a>Objeto Product

El **objeto Product** representa una instancia única de un producto anunciado, instalado o desconocido.

Se puede crear una instancia del objeto con la propiedad **Product** como "WindowsInstaller.Installer.Product(*ProductCode*, *UserSid*, *Context*)". *UserSid* debe ser NULL para el contexto por equipo. *UserSid* puede ser NULL para el usuario actual especificado, cuando el contexto no es por equipo. *Se requieren los* *parámetros* ProductCode y Context.

## <a name="members"></a>Miembros

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



| Propiedad                                                      | Descripción                                                                                 |
|:--------------------------------------------------------------|:--------------------------------------------------------------------------------------------|
| [**ComponentState**](product-componentstate.md)<br/>   | Estado de un componente especificado para esta instancia de producto. <br/>                   |
| [**Contexto**](product-context.md)<br/>                 | Contexto de esta instancia de producto como un valor MSIINSTALLCONTEXT. <br/>                 |
| [**FeatureState**](product-featurestate.md)<br/>       | Estado de una característica especificada para esta instancia de producto. <br/>                     |
| [**InstallProperty**](product-installproperty.md)<br/> | Valor de una propiedad especificada. <br/>                                              |
| [**MediaDisks**](product-mediadisks.md)<br/>           | Enumera todos los discos multimedia de esta instancia de producto.<br/>                        |
| [**ProductCode**](product-productcode.md)<br/>         | Devuelve el código del producto. <br/>                                                       |
| [**SourceListInfo**](product-sourcelistinfo.md)<br/>   | Obtiene y establece las propiedades de información de origen. Se trata de una propiedad de lectura o escritura.<br/> |
| [**Orígenes**](product-sources.md)<br/>                 | Enumera todos los orígenes de esta instancia de producto.<br/>                            |
| [**Estado**](product-state.md)<br/>                     | Estado de instalación del producto.<br/>                                               |
| [**UserSid**](product-usersid.md)<br/>                 | Devuelve el SID de usuario, con la cuenta en la que está disponible esta instancia del producto.<br/>    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador 3.0 o posterior en Windows Server 2003, Windows XP y Windows 2000<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                                                   |
| IID<br/>     | IID IProduct se define como \_ 000C10A0-0000-0000-C000-000000000046<br/>                                                                                                                                                                                                          |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




