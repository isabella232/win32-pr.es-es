---
title: Estructura de ORPC_DBG_BUFFER
description: La \_ \_ estructura de búfer ORPC dbg es el formato de búfer utilizado para calcular las referencias de los datos RPC a los métodos de la interfaz IOrpcDebugNotify.
ms.assetid: 444cd3b8-bc7b-425d-9ccc-04fd6c7393b2
keywords:
- Estructura de ORPC_DBG_BUFFER COM
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
ms.openlocfilehash: 4dc42251b928207a2b009a18c1d88e94dcf1492a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105695889"
---
# <a name="orpc_dbg_buffer-structure"></a>ORPC \_ \_ estructura de búfer dbg

La estructura de **\_ \_ búfer ORPC dbg** es el formato de búfer utilizado para calcular las referencias de los datos RPC a los métodos de la interfaz [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

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



| Value                                                                                                                                                                                                                                                                   | Significado                                                                                                                                                                                                                                        |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ORPC_DEBUG_ALWAYS"></span><span id="orpc_debug_always"></span><dl> <dt>**ORPC \_ Depurar \_ siempre**</dt> <dt>0x00000000</dt> </dl>                              | Si se establece, COM siempre generará la notificación de cliente o servidor en el receptor.<br/>                                                                                                                                                    |
| <span id="ORPC_DEBUG_IF_HOOK_ENABLED"></span><span id="orpc_debug_if_hook_enabled"></span><dl> <dt>**ORPC \_ Depurar \_ si el \_ enlace \_ está habilitado**</dt> <dt>0x00000001</dt> </dl> | Si se establece, COM solo generará la notificación de cliente o de servidor en el receptor si se ha habilitado la depuración de COM mediante una llamada a [**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md) en ese proceso con **FTrace** establecido en **true**. <br/> |



 

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

El número de bytes, incluido **cbRemaining**, que siguen en esta estructura.

</dd> <dt>

**guidSemantic**
</dt> <dd>

Un GUID que determina qué miembros de la Unión están presentes a continuación. **guidSemantic** puede tomar uno de los siguientes valores:



| Value                                                                                                           | Significado                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>9CADE560-8F43-101A-B07B-00DD01113F11</dt> </dl> | Determina si el depurador realiza una ejecución paso a paso. A continuación solo está presente el miembro **fStopOnOtherSide** de la Unión.<br/>                                             |
| <dl> <dt>D62AEDFA-57EA-11ce-A964-00AA006C3706</dt> </dl> | Determina si los datos de serialización RPC y los códigos de la depuración se pasan al receptor. Todos los miembros de la Unión están presentes a continuación con la excepción de **fStopOnOtherSide**.<br/> |



 

</dd> <dt>

**fStopOnOtherSide**
</dt> <dd>

Si es **true**, el depurador realiza una ejecución paso a paso y debe salir del servidor y continuar la ejecución una vez que se alcanza el otro lado. De lo contrario, no se realiza una ejecución paso a paso y la ejecución del depurador se detiene en el otro lado.

</dd> <dt>

**wDebuggingOpCode**
</dt> <dd>

Un valor que permite especificar una serie de operaciones. **wDebuggingOpCode** puede tomar uno de los siguientes valores:



| Value                                                                             | Significado                                                                                              |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>0x0000</dt> </dl> | No hay ninguna operación.<br/>                                                                             |
| <dl> <dt>0x0001</dt> </dl> | Si se establece, la semántica de un solo paso es idéntica a **fStopOnOtherSide** cuando se establece en **true**.<br/> |



 

</dd> <dt>

**cExtent**
</dt> <dd>

Acolcha. No debe usarse.

</dd> <dt>

**padding**
</dt> <dd>

Acolcha. No debe usarse.

</dd> <dt>

**CB**
</dt> <dd>

Tamaño, en bytes, de los datos de **rgbData**.

</dd> <dt>

**guidExtent**
</dt> <dd>

Un **GUID** que determina el tipo de datos en **rgbData**. **guidExtent** puede tomar uno de los siguientes valores:



| Value                                                                                                           | Significado                                                   |
|-----------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <dt>53199051-57EB-11ce-A964-00AA006C3706</dt> </dl> | **rgbData** es un puntero de interfaz de cálculo de referencias.<br/> |



 

</dd> <dt>

**rgbData**
</dt> <dd>

Búfer de **bytes** que se usa para pasar datos com de cálculo de referencias RPC entre los depuradores de cliente y de servidor. El contenido de **rgbData** viene determinado por el **GUID** de **guidExtent**.



| Valor guidExtent                     | contenido de rgbData                                                                                                                                                                                                                                    |
|--------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 53199051-57EB-11ce-A964-00AA006C3706 | Puntero de interfaz de cálculo de referencias que es el resultado de llamar a [**CoMarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-comarshalinterface). El puntero de cálculo de referencias se convierte en su puntero de interfaz correspondiente mediante [**CoUnmarshalInterface**](/windows/desktop/api/combaseapi/nf-combaseapi-counmarshalinterface). |



 

</dd> </dl>

## <a name="remarks"></a>Observaciones

Estos miembros de esta estructura tienen una alineación de 1 byte y se transmiten siempre en orden de bytes Little-Endian.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                     |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                           |
| Encabezado<br/>                   | <dl> <dt>N/D</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ORPC \_ dbg \_ All**](orpc-dbg-all.md)
</dt> <dt>

[**ORPC \_ init \_ args**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

 





