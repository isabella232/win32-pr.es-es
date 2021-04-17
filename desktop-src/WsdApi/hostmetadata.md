---
description: Define los metadatos de hospedaje para el dispositivo que se va a implementar. Este elemento se usa solo para implementaciones de dispositivos (hosts).
ms.assetid: ca7bc5ea-8ab2-4233-86d2-5b793021b8ee
title: elemento hostMetadata
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: becd6bc3eab6b1aa1d95414c6348288e0d29dbd0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105659975"
---
# <a name="hostmetadata-element"></a>elemento hostMetadata

Define los metadatos de hospedaje para el dispositivo que se va a implementar. Este elemento se usa solo para implementaciones de dispositivos (hosts).

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
| [**organizar**](host.md)<br/>     | Define los elementos ServiceID y [**Types**](types.md) para el host de servicio. Si no se proporciona explícitamente, WSDAPI no proporcionará datos predeterminados en respuesta a las solicitudes de metadatos.<br/> <br/>                                                                                                                                          |
| [**ubicada**](hosted.md)<br/> | Define los elementos [**ServiceID**](serviceid.md) y [**Types**](types.md) para los servicios proporcionados por este host de servicio. Cada servicio proporcionado por este host de servicio debe tener su propia información de elemento [**hospedado**](hosted.md) para asegurarse de que el servicio se publique correctamente en las respuestas a las solicitudes de metadatos.<br/> <br/> |



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

Los metadatos de hospedaje aparecen en este elemento en un formato similar al especificado en el perfil de dispositivo. **hostMetadata** es ligeramente diferente del formato descrito en el perfil de dispositivo, ya que la única propiedad de referencia que admite es el identificador de servicio.

El elemento [**relationshipMetadataDefinition**](relationshipmetadatadefinition.md) se usa posteriormente para generar una constante de C que contiene esta información.

## <a name="element-information"></a>Información de elemento



|                                     |               |
|-------------------------------------|---------------|
| Sistema mínimo compatible<br/> | Windows Vista |
| Puede estar vacío                        | No            |



 

 




