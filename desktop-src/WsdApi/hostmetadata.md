---
description: Define los metadatos de hospedaje del dispositivo que se va a implementar. Este elemento solo se usa para implementaciones de dispositivos (hosts).
ms.assetid: ca7bc5ea-8ab2-4233-86d2-5b793021b8ee
title: elemento hostMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d9cf6fa139a2723ed90dfe281fc7b054016386fa
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126966980"
---
# <a name="hostmetadata-element"></a>elemento hostMetadata

Define los metadatos de hospedaje del dispositivo que se va a implementar. Este elemento solo se usa para implementaciones de dispositivos (hosts).

## <a name="usage"></a>Uso

``` syntax
<hostMetadata>
  child elements
</hostMetadata>
```

## <a name="attributes"></a>Atributos

No hay atributos.

## <a name="child-elements"></a>Elementos secundarios



| Elemento                             | Descripción                                                                                                                                                                                                                                                                                                                                           |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Host**](host.md)<br/>     | Define los elementos ServiceID y [**Types**](types.md) para el host de servicio. Si no se proporciona explícitamente, WSDAPI no suministrará ningún dato predeterminado en respuesta a las solicitudes de metadatos.<br/> <br/>                                                                                                                                          |
| [**Alojados**](hosted.md)<br/> | Define los [**elementos ServiceID**](serviceid.md) y [**Types**](types.md) para los servicios proporcionados por este host de servicio. Cada servicio proporcionado por este host [](hosted.md) de servicio debe tener su propia información de elemento hospedado para asegurarse de que el servicio se publica correctamente en respuestas a solicitudes de metadatos.<br/> <br/> |



### <a name="child-element-sequence"></a>Secuencia de elementos secundarios

``` syntax
(
  host?, 
  hosted+
)
```

## <a name="parent-elements"></a>Elementos primarios



| Elemento                                                         | Descripción                                                                   |
|-----------------------------------------------------------------|-------------------------------------------------------------------------------|
| [**relationshipMetadata**](relationshipmetadata.md)<br/> | Describe el host y los metadatos hospedados para el dispositivo.<br/> <br/> |



## <a name="remarks"></a>Observaciones

Los metadatos de hospedaje aparecen en este elemento con un formato similar al especificado en el perfil de dispositivo. **hostMetadata** es ligeramente diferente del formato descrito en el perfil de dispositivo en que la única propiedad de referencia que admite es el identificador de servicio.

El [**elemento relationshipMetadataDefinition**](relationshipmetadatadefinition.md) se usa posteriormente para generar una constante de C que contiene esta información.

## <a name="element-information"></a>Información de elemento



| Etiqueta | Value |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | No            |



 

 




