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
ms.openlocfilehash: 136bc160ea81367f8f55ad81cfc06f5e2e272cafae9d7b8f444a65d34e85d52b
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119328375"
---
# <a name="featureinfo-object"></a>Objeto FeatureInfo

El **objeto FeatureInfo** contiene información sobre la característica de destino y se crea a partir del [**objeto Session**](session-object.md) mediante el método [**FeatureInfo.**](session-featureinfo.md)

## <a name="members"></a>Miembros

El **objeto FeatureInfo** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

El **objeto FeatureInfo** tiene estas propiedades.



| Propiedad                                                  | Tipo de acceso           | Descripción                                                                                 |
|:----------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------|
| [**Atributos**](featureinfo-attributes.md)<br/>   | Lectura/escritura<br/> | Devuelve el valor de la característica en la columna Atributos de la tabla Característica.<br/> |
| [**Descripción**](featureinfo-description.md)<br/> |                       | Devuelve la descripción de la característica.<br/>                                          |
| [**Título**](featureinfo-title.md)<br/>             | Solo lectura<br/>  | Devuelve el título de la característica.<br/>                                                |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Instalador 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ IFeatureInfo se define como 000C109F-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




