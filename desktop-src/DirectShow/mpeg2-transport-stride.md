---
description: La \_ \_ estructura de intervalo de transporte de MPEG2 describe el formato de los paquetes de secuencias de transporte MPEG-2 (TS).
ms.assetid: 269d5fba-2dea-4786-93d6-e52b56c8bb53
title: MPEG2_TRANSPORT_STRIDE estructura (Bdatypes. h)
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
ms.openlocfilehash: 4a0cdc21bdd8c320728da0c0af8c0af023de68eb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690073"
---
# <a name="mpeg2_transport_stride-structure"></a>Estructura de intervalo de \_ transporte de MPEG2 \_

La `MPEG2_TRANSPORT_STRIDE` estructura describe el formato de los paquetes de secuencias de transporte MPEG-2 (TS). Esta estructura permite transportes de flujos en los que los paquetes de transporte de 188 bytes no son contiguos. En esta documentación, se hace referencia a estos paquetes como *paquetes STRIDE*.

Los paquetes STRIDE se identifican con el siguiente tipo de medio:



|             |                                        |
|-------------|----------------------------------------|
| Tipo principal  | \_Secuencia MEDIATYPE                      |
| Subtype     | \_Intervalo de \_ transporte de MPEG2 de MEDIASUBTYPE \_ |
| Tipo de formato | FORMATO \_ ninguno                           |



 

El bloque de formato (**pbFormat**) es opcional. Si se incluye el bloque de formato, debe comenzar con una estructura de **\_ \_ intervalo de transporte de MPEG2** . Esta estructura define el diseño del paquete de transporte en el paquete STRIDE. Si el bloque de formato es **null**, se supone que los paquetes usan un conjunto de valores predeterminados. Vea la sección Comentarios para obtener más información.

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

Especifica el desplazamiento, en bytes, desde el principio del paquete hasta el primer byte del paquete de transporte incrustado. El valor debe estar comprendido entre cero y `(dwStride - dwPacketLength)` , ambos inclusive.

</dd> <dt>

**dwPacketLength**
</dt> <dd>

Especifica la longitud del paquete de transporte incrustado, en bytes. En el caso de los paquetes de transporte MPEG-2 estándar, el valor debe ser 188 bytes.

</dd> <dt>

**dwStride**
</dt> <dd>

Especifica la longitud de todo el paquete STRIDE, en bytes. El valor debe ser al menos `(dwOffset + dwPacketLength)` .

</dd> </dl>

## <a name="remarks"></a>Observaciones

En el siguiente diagrama se ilustran las relaciones entre los miembros de la estructura.

![paquete de paso MPEG-2](images/mpeg2-stride-packet.png)

Los búferes de entrada que contienen paquetes de intervalo multiplexado tienen algunas restricciones:

-   Los paquetes STRIDE deben empaquetarse de forma contigua en el búfer.
-   Ningún byte puede preceder al primer paquete STRIDE o seguir el último paquete STRIDE.
-   Un número entero de paquetes STRIDE debe caber en el búfer; es decir, la longitud del búfer% dwStride es igual a cero.

No hay ninguna restricción en el número de paquetes STRIDE por búfer.

Si el tipo de medio no contiene un bloque de formato (**pbFormat** es **null**), se usan los siguientes valores predeterminados:

-   **dwOffset**: 0
-   **dwPacketLength**: 188
-   **dwStride**: 188

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Bdatypes. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Estructuras de DirectShow](directshow-structures.md)
</dt> <dt>

[Tipos de medios MPEG-2](mpeg-2-media-types.md)
</dt> </dl>

 

 




