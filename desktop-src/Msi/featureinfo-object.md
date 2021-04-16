---
description: El objeto FeatureInfo contiene información sobre la característica de destino y se crea a partir del objeto de sesión mediante el método FeatureInfo.
ms.assetid: c9c96799-22c7-4e74-947b-3b8d31ebc1f1
title: Objeto FeatureInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FeatureInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 1db1bab5b1e55f027bb01eb9eff22484a4e39170
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670350"
---
# <a name="featureinfo-object"></a>Objeto FeatureInfo

El objeto **FeatureInfo** contiene información sobre la característica de destino y se crea a partir del objeto de [**sesión**](session-object.md) mediante el método [**FeatureInfo**](session-featureinfo.md) .

## <a name="members"></a>Miembros

El objeto **FeatureInfo** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El objeto **FeatureInfo** tiene estas propiedades.



| Propiedad                                                  | Tipo de acceso           | Descripción                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**Atributos**](featureinfo-attributes.md)<br/>   | Lectura/escritura<br/> | Devuelve el valor de la característica en la columna Attributes de la tabla de características.<br/> |
| [**Descripción**](featureinfo-description.md)<br/> |                       | Devuelve la descripción de la característica.<br/>                                          |
| [**Title**](featureinfo-title.md)<br/>             | Solo lectura<br/>  | Devuelve el título de la característica.<br/>                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IFeatureInfo se define como 000C109F-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Ejemplos de scripting Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




