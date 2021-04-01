---
title: Estructura MrmResourceIndexerMessage (MrmResourceIndexer. h)
description: Representa un mensaje generado por un indizador de recursos. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados.
ms.assetid: E00065E6-A468-4ACD-AF89-434E4F5025A4
keywords:
- Menús de la estructura MrmResourceIndexerMessage y otros recursos
- PMrmResourceIndexerMessage menús de puntero de estructura y otros recursos
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
ms.openlocfilehash: 5073c4f74852d341d7f0711a34abe4459dcbaa79
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996069"
---
# <a name="mrmresourceindexermessage-structure"></a>Estructura MrmResourceIndexerMessage

\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial. Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]

Representa un mensaje generado por un indizador de recursos. Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).

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

**id**
</dt> <dd>

Tipo: **ULong**

</dd> <dd>

Identificador único del mensaje.

</dd> <dt>

**text**
</dt> <dd>

Tipo: **PCWSTR**

</dd> <dd>

Texto del mensaje. No libere este puntero; la memoria es propiedad del sistema operativo.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 10, versión 1803 \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server \[\]<br/>                                                 |
| Encabezado<br/>                   | <dl> <dt>MrmResourceIndexer. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems)
</dt> </dl>

 

