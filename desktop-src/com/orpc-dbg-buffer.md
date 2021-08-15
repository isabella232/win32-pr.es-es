---
title: ORPC_DBG_BUFFER estructura
description: La estructura BUFFER de DBG DE ORPC es el formato de búfer que se usa para canalizar datos RPC a los métodos de \_ \_ la interfaz IOrpcDebugNotify.
ms.assetid: 444cd3b8-bc7b-425d-9ccc-04fd6c7393b2
keywords:
- ORPC_DBG_BUFFER com de estructura
- PORPC_DBG_BUFFER puntero de estructura COM
topic_type:
- apiref
api_name:
- ORPC_DBG_BUFFER
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cb1f83cfcbe673cd2d5701e57ae1e94d4e04b59b845cd9ec7b617077da24bb0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310261"
---
# <a name="orpc_dbg_buffer-structure"></a>ESTRUCTURA DE \_ BÚFER DE DBG DE ORPC \_

La **estructura BUFFER de \_ DBG \_ DE ORPC** es el formato de búfer que se usa para canalizar datos RPC a los métodos de la [**interfaz IOrpcDebugNotify.**](iorpcdebugnotify.md)

## <a name="syntax"></a>Sintaxis


```C++
typedef struct _ORPC_DBG_BUFFER {
  DWORD alwaysOrSometimes;
  BYTE  verMajor;
  BYTE  verMinor;
  DWORD cbRemaining;
  GUID  guidSemantic;
  union {
    BOOL   fStopOnOtherSide;
    USHORT wDebuggingOpCode;
    USHORT cExtent;
    BYTE   padding[2];
    struct {
      ULONG cb;
      GUID  guidExtent;
      BYTE  *rgbData;
    };
  };
} ORPC_DBG_BUFFER, *PORPC_DBG_BUFFER;
```



## <a name="members"></a>Miembros

<dl> <dt>

**alwaysOrSometimes**
</dt> <dd>

Valor que controla la generación del depurador. **alwaysOrSometimes** puede ser uno de los siguientes valores:



| Valor                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ORPC_DEBUG_ALWAYS"></span><span id="orpc_debug_always"></span><dl> <dt>**ORPC \_ DEPURAR \_ SIEMPRE**</dt> <dt>0x00000000</dt> </dl>                              | Si se establece, COM siempre genera la notificación de cliente o servidor en el receptor.<br/>                                                                                                                                                    |
| <span id="ORPC_DEBUG_IF_HOOK_ENABLED"></span><span id="orpc_debug_if_hook_enabled"></span><dl> <dt>**ORPC \_ DEPURACIÓN \_ SI \_ EL ENLACE \_ ESTÁ**</dt> <dt>0X00000001</dt> </dl> | Si se establece, COM solo genera la notificación de cliente o servidor en el receptor si se ha habilitado la depuración COM mediante una llamada a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) en ese proceso con **fTrace** establecido en **TRUE.** <br/> |



 

</dd> <dt>

**verMajor**
</dt> <dd>

Número de versión principal de la especificación de formato de datos.

</dd> <dt>

**verMinor**
</dt> <dd>

Número de versión secundaria de la especificación de formato de datos.

</dd> <dt>

**cbRemaining**
</dt> <dd>

Número de bytes, incluido **cbRemaining**, que siguen a esta estructura.

</dd> <dt>

**guidSemantic**
</dt> <dd>

Guid que determina qué miembros de la unión están presentes a continuación. **guidSemantic** puede tomar uno de los siguientes valores:



| Valor                                                                                                           | Significado                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt> </dl> | Determina si el depurador va a realizar una sola ejecución paso a paso. A continuación solo está presente el miembro **fStopOnOtherSide** de la unión.<br/>                                             |
| <dl> <dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt> </dl> | Determina si se pasan al receptor los datos y códigos de operación de depuración de RPC. Todos los miembros de la unión están presentes a continuación, a excepción de **fStopOnOtherSide**.<br/> |



 

</dd> <dt>

**fStopOnOtherSide**
</dt> <dd>

Si **es TRUE,** el depurador realiza una sola ejecución paso a paso y debe salir del servidor y continuar con la ejecución una vez que se alcanza el otro lado. De lo contrario, no se realiza una sola ejecución y la ejecución del depurador se detiene en el otro lado.

</dd> <dt>

**wDebuggingOpCode**
</dt> <dd>

Valor que permite especificar una de una serie de operaciones. **wDebuggingOpCode** puede tomar uno de los siguientes valores:



| Valor                                                                             | Significado                                                                                              |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x0000</dt> </dl> | No hay ninguna operación.<br/>                                                                             |
| <dl> <dt>0x0001</dt> </dl> | Si se establece, la semántica de un solo paso es idéntica **a fStopOnOtherSide cuando** se establece en **TRUE.**<br/> |



 

</dd> <dt>

**cExtent**
</dt> <dd>

Acolchado. No debe usarse.

</dd> <dt>

**padding**
</dt> <dd>

Acolchado. No debe usarse.

</dd> <dt>

**Cb**
</dt> <dd>

Tamaño, en bytes de los datos en **rgbData**.

</dd> <dt>

**guidExtent**
</dt> <dd>

GUID **que** determina el tipo de datos en **rgbData.** **guidExtent** puede tomar uno de los siguientes valores:



| Valor                                                                                                           | Significado                                                   |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>53199051-57EB-11ce-A964-00AA006C3706</dt> </dl> | **rgbData es** un puntero de interfaz de tipo marshalled.<br/> |



 

</dd> <dt>

**rgbData**
</dt> <dd>

Búfer **BYTE** que se usa para pasar datos COM con cifrado RPC entre los depuradores de cliente y servidor. El contenido de **rgbData** viene determinado por el **GUID** en **guidExtent.**



| Valor guidExtent                     | contenido rgbData                                                                                                                                                                                                                                    |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 53199051-57EB-11ce-A964-00AA006C3706 | Puntero de interfaz de referencia que resulta de llamar a [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface). El puntero de referencia se convierte en su puntero de interfaz correspondiente mediante [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface). |



 

</dd> </dl>

## <a name="remarks"></a>Comentarios

Estos miembros de esta estructura tienen una alineación de 1 byte y siempre se transmiten en orden de bytes little-endian.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                     |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                           |
| Encabezado<br/>                   | <dl> <dt>N/D</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ORPC \_ DBG \_ ALL**](orpc-dbg-all.md)
</dt> <dt>

[**ORPC \_ INIT \_ ARGS**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 





