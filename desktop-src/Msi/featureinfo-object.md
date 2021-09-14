---
description: El objeto FeatureInfo contiene información sobre la característica de destino y se crea a partir del objeto Session mediante el método FeatureInfo.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074810"
---
# <a name="featureinfo-object"></a>Objeto FeatureInfo

El **objeto FeatureInfo** contiene información sobre la característica de destino y se crea a partir del [**objeto Session**](session-object.md) mediante el método [**FeatureInfo.**](session-featureinfo.md)

## <a name="members"></a>Members

El **objeto FeatureInfo** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto FeatureInfo** tiene estas propiedades.



| Propiedad.                                                  | Tipo de acceso           | Descripción                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**Atributos**](featureinfo-attributes.md)<br/>   | Lectura y escritura<br/> | Devuelve el valor de la característica en la columna Atributos de la tabla Característica.<br/> |
| [**Descripción**](featureinfo-description.md)<br/> |                       | Devuelve la descripción de la característica.<br/>                                          |
| [**Título**](featureinfo-title.md)<br/>             | Solo lectura<br/>  | Devuelve el título de la característica.<br/>                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IFeatureInfo se define como 000C109F-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




