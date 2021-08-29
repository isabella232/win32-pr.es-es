---
title: Estructura MrmResourceIndexerMessage (MrmResourceIndexer.h)
description: Representa un mensaje generado por un indexador de recursos. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, consulte API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: E00065E6-A468-4ACD-AF89-434E4F5025A4
keywords:
- Menús de estructura MrmResourceIndexerMessage y otros recursos
- Menús de puntero de estructura PMrmResourceIndexerMessage y otros recursos
topic_type:
- apiref
api_name:
- MrmResourceIndexerMessage
api_location:
- MrmResourceIndexer.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54751d11816a121ca9a7678a431219f6c12a8bf103c314420f739948d97e8f38
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939775"
---
# <a name="mrmresourceindexermessage-structure"></a>Estructura MrmResourceIndexerMessage

\[Parte de la información está relacionada con el producto publicado previamente que puede modificarse considerablemente antes de su lanzamiento comercial. Microsoft no otorga ninguna garantía, explícita o implícita, con respecto a la información proporcionada aquí.\]

Representa un mensaje generado por un indexador de recursos. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, consulte API de indexación de recursos de paquetes (PRI) y sistemas [de compilación personalizados.](/windows/uwp/app-resources/pri-apis-custom-build-systems)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _MrmResourceIndexerMessage {
  MrmResourceIndexerMessageSeverity severity;
  ULONG                             id;
  PCWSTR                            text;
} MrmResourceIndexerMessage, *PMrmResourceIndexerMessage;
```



## <a name="members"></a>Miembros

<dl> <dt>

**severity**
</dt> <dd>

Tipo: **[ **MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md)**

</dd> <dd>

Valor que indica la gravedad del mensaje.

</dd> <dt>

**identificador**
</dt> <dd>

Tipo: **ULONG**

</dd> <dd>

Identificador único para el mensaje.

</dd> <dt>

**text**
</dt> <dd>

Tipo: **PCWSTR**

</dd> <dd>

Texto del mensaje. No liberar este puntero; la memoria es propiedad del sistema operativo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 10, solo aplicaciones de escritorio de la versión 1803 \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de servidor\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>MrmResourceIndexer.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

