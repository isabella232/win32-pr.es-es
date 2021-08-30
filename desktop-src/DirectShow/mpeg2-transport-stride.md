---
description: La estructura MPEG2 TRANSPORT STRIDE describe el formato de los paquetes de flujo de transporte \_ \_ MPEG-2 (TS).
ms.assetid: 269d5fba-2dea-4786-93d6-e52b56c8bb53
title: MPEG2_TRANSPORT_STRIDE estructura (Bdatypes.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MPEG2_TRANSPORT_STRIDE
api_type:
- HeaderDef
api_location:
- bdatypes.h
ms.openlocfilehash: eaea633aa543c4b8fa2ddaf95f0914b759eb5f75bf2352f55e5811766d4e001d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120051045"
---
# <a name="mpeg2_transport_stride-structure"></a>Estructura MPEG2 \_ TRANSPORT \_ STRIDE

La estructura describe el formato de los paquetes de flujo de transporte `MPEG2_TRANSPORT_STRIDE` MPEG-2 (TS). Esta estructura permite los flujos de transporte en los que los paquetes de transporte de 188 bytes no son contiguos. Para esta documentación, estos paquetes se conocen como *paquetes de paso* a paso.

Los paquetes stride se identifican mediante el siguiente tipo de medio:



| Etiqueta | Value |
|-------------|----------------------------------------|
| Tipo principal  | Secuencia \_ MEDIATYPE                      |
| Subtype     | MEDIASUBTYPE \_ MPEG2 \_ TRANSPORT \_ STRIDE |
| Tipo de formato | FORMAT \_ None                           |



 

El bloque de formato (**pbFormat**) es opcional. Si se incluye el bloque de formato, debe comenzar con una estructura **MPEG2 \_ TRANSPORT \_ STRIDE.** Esta estructura define el diseño del paquete de transporte dentro del paquete stride. Si el bloque de formato **es NULL,** se supone que los paquetes usan un conjunto de valores predeterminados; consulte la sección Comentarios para obtener más información.

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _MPEG2_TRANSPORT_STRIDE {
  DWORD dwOffset;
  DWORD dwPacketLength;
  DWORD dwStride;
} MPEG2_TRANSPORT_STRIDE, *PMPEG2_TRANSPORT_STRIDE;
```



## <a name="members"></a>Miembros

<dl> <dt>

**dwOffset**
</dt> <dd>

Especifica el desplazamiento, en bytes, desde el principio del paquete hasta el primer byte del paquete de transporte incrustado. El valor debe oscilar entre cero y `(dwStride - dwPacketLength)` , ambos inclusive.

</dd> <dt>

**dwPacketLength**
</dt> <dd>

Especifica la longitud del paquete de transporte incrustado, en bytes. Para los paquetes de transporte MPEG-2 estándar, el valor debe ser de 188 bytes.

</dd> <dt>

**dwStride**
</dt> <dd>

Especifica la longitud del paquete stride completo, en bytes. El valor debe ser al menos `(dwOffset + dwPacketLength)` .

</dd> </dl>

## <a name="remarks"></a>Comentarios

En el diagrama siguiente se muestran las relaciones entre los miembros de la estructura.

![paquete mpeg-2 stride](images/mpeg2-stride-packet.png)

Los búferes de entrada que contienen paquetes de pasos multiplexados tienen algunas restricciones:

-   Los paquetes stride deben empaquetarse de forma contigua dentro del búfer.
-   Ningún bytes puede preceder al primer paquete de pasos o seguir el último paquete de pasos.
-   Un número entero de paquetes de pasos debe caber en el búfer; es decir, la longitud del búfer % dwStride es igual a cero.

No hay ninguna restricción en el número de paquetes de pasos por búfer.

Si el tipo de medio no contiene un bloque de formato **(pbFormat** es **NULL),** se usan los siguientes valores predeterminados:

-   **dwOffset:** 0
-   **dwPacketLength:** 188
-   **dwStride:** 188

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Bdatypes.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[DirectShow Estructuras](directshow-structures.md)
</dt> <dt>

[Tipos de medios MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 




