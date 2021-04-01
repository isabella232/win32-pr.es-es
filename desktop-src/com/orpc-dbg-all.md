---
title: Estructura de ORPC_DBG_ALL
description: La \_ estructura ORPC dbg \_ All se usa para pasar parámetros a los métodos de la interfaz IOrpcDebugNotify.
ms.assetid: 05371beb-9202-40a6-96d2-4b91497e2ee9
keywords:
- Estructura de ORPC_DBG_ALL COM
- LPORPC_DBG_ALL puntero de estructura COM
topic_type:
- apiref
api_name:
- ORPC_DBG_ALL
api_location:
- N/A
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a17f5b09e5fe2f668bf2bcd21e2e7fe6f0f766a7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150083"
---
# <a name="orpc_dbg_all-structure"></a>ORPC \_ dbg \_ All (estructura)

La estructura **ORPC \_ dbg \_ All** se usa para pasar parámetros a los métodos de la interfaz [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

> [!Note]  
> Cada método de la interfaz [**IOrpcDebugNotify**](iorpcdebugnotify.md) utiliza una combinación diferente de los miembros siguientes. Si un miembro no se indica como lo usa un método, no está definido cuando se pasa a ese método.

 

## <a name="syntax"></a>Sintaxis


```C++
typedef struct ORPC_DBG_ALL {
  BYTE              *pSignature;
  RPCOLEMESSAGE     *pMessage;
  const IID         *refiid;
  IRpcChannelBuffer *pChannel;
  IUnknown          *pUnkProxyMgr;
  void              *pInterface;
  IUnknown          *pUnkObject;
  HRESULT           hresult;
  void              *pvBuffer;
  ULONG             *cbBuffer;
  ULONG             *lpcbBuffer;
  void              *reserved;
} ORPC_DBG_ALL, *LPORPC_DBG_ALL;
```



## <a name="members"></a>Miembros

<dl> <dt>

**pSignature**
</dt> <dd>

Un puntero a un búfer de **bytes** que contiene:

-   Primeros cuatro bytes: los caracteres ASCII "MARB" al aumentar el orden de la memoria.
-   16 bytes siguientes: un **GUID** que identifica la notificación a la que se llama. Contiene uno de los siguientes:
    1.  [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): 9ED14F80-9673-101A-B07B-00DD01113F11
    2.  [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):D a45f3e0-9673-101A-B07B-00DD01113F11
    3.  [**ClientNotify**](iorpcdebugnotify-clientnotify.md): 4F60E540-9674-101A-B07B-00DD01113F11
    4.  [**ServerNotify**](iorpcdebugnotify-servernotify.md): 1084FA00-9674-101A-B07B-00DD01113F11
    5.  [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): 22080240-9674-101A-B07B-00DD01113F11
    6.  [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md): 2FC09500-9674-101A-B07B-00DD01113F11
-   Siguientes cuatro bytes: reservado para uso futuro.

> [!Note]
>
> Lo usan todos los métodos de la interfaz [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

 

</dd> <dt>

**pMessage**
</dt> <dd>

Puntero a una estructura [**RPCOLEMESSAGE**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) que contiene información de cálculo de referencias de datos RPC.

> [!Note]
>
> Lo usan los métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)y [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**REFIID**
</dt> <dd>

Puntero al IID de la interfaz [**IOrpcDebugNotify**](iorpcdebugnotify.md) .

> [!Note]
>
> Lo usan los métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)y [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**pChannel**
</dt> <dd>

Puntero a la interfaz [**IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) de la implementación del canal RPC de com en el servidor.

> [!Note]
>
> Lo usan los métodos [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)y [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**pUnkProxyMgr**
</dt> <dd>

Puntero a la interfaz [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) del objeto implicado en esta invocación del depurador. Sin embargo, puede ser **null**, lo que reduce la funcionalidad del depurador.

> [!Note]
>
> Lo usan los métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)y [**ClientNotify**](iorpcdebugnotify-clientnotify.md) .

 

</dd> <dt>

**pInterface**
</dt> <dd>

Puntero a la interfaz COM del método que va a invocar esta RPC. No debe ser **null**.

> [!Note]
>
> Lo usan los métodos [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)y [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**pUnkObject**
</dt> <dd>

Debe ser **null**.

> [!Note]
>
> Lo usan los métodos [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)y [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**valor**
</dt> <dd>

El propósito de este miembro cambia para cada una de las notificaciones siguientes:

[**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md): el número de bytes que el depurador del cliente transmitirá al depurador del servidor. Si es cero, no es necesario transmitir información.

[**ClientNotify**](iorpcdebugnotify-clientnotify.md): **HRESULT** de la última RPC.

[**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md): el número de bytes que el depurador del cliente transmitirá al depurador del servidor. Si es cero, no es necesario transmitir información.

> [!Note]
>
> Lo usan los métodos [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md)y [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md) .

 

</dd> <dt>

**pvBuffer**
</dt> <dd>

Puntero a una estructura [**de \_ \_ búfer de ORPC dbg**](orpc-dbg-buffer.md) que contiene la información de depuración de serialización de RPC. Es indefinido si **cbBuffer** es cero.

> [!Note]
>
> Lo usan los métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)y [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**cbBuffer**
</dt> <dd>

La longitud, en bytes, de los datos a los que apunta **pvBuffer**.

> [!Note]
>
> Lo usan los métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)y [**ServerNotify**](iorpcdebugnotify-servernotify.md) .

 

</dd> <dt>

**lpcbBuffer**
</dt> <dd>

El número de bytes que el depurador del cliente transmitirá al depurador del servidor. Si es cero, no es necesario transmitir información. Este valor reemplaza el valor devuelto en **HRESULT**.

> [!Note]
>
> Lo usan los métodos [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md) .

 

</dd> <dt>

**sector**
</dt> <dd>

Reservado. No utilizar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                     |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                           |
| Encabezado<br/>                   | <dl> <dt>N/D</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**\_búfer ORPC dbg \_**](orpc-dbg-buffer.md)
</dt> <dt>

[**ORPC \_ init \_ args**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

