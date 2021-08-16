---
title: ORPC_DBG_ALL estructura
description: La estructura ORPC DBG ALL se usa para pasar parámetros a \_ \_ los métodos de la interfaz IOrpcDebugNotify.
ms.assetid: 05371beb-9202-40a6-96d2-4b91497e2ee9
keywords:
- ORPC_DBG_ALL com de estructura
- LPORPC_DBG_ALL de estructura de datos COM
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
ms.openlocfilehash: 359e3b3ec2530917c6a502da90ea86771238319687f8dcf8e9b7862e4ddf1954
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118310309"
---
# <a name="orpc_dbg_all-structure"></a>ESTRUCTURA ORPC \_ DBG \_ ALL

La **estructura ORPC \_ DBG \_ ALL** se usa para pasar parámetros a los métodos de la [**interfaz IOrpcDebugNotify.**](iorpcdebugnotify.md)

> [!Note]  
> Cada método de la [**interfaz IOrpcDebugNotify**](iorpcdebugnotify.md) usa una combinación diferente de los miembros siguientes. Si un miembro no se indica como utilizado por un método, no se define cuando se pasa a ese método.

 

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

Puntero a un búfer **BYTE** que contiene:

-   Primeros cuatro bytes: los caracteres ASCII "MARB" en orden de memoria creciente.
-   16 bytes siguientes: **GUID** que identifica la notificación a la que se llama. Contiene uno de los siguientes elementos:
    1.  [**ClientGetBufferSize:**](iorpcdebugnotify-clientgetbuffersize.md)9ED14F80-9673-101A-B07B-00DD01113F11
    2.  [**ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md):D A45F3E0-9673-101A-B07B-00DD01113F11
    3.  [**ClientNotify**](iorpcdebugnotify-clientnotify.md):4F60E540-9674-101A-B07B-00DD01113F11
    4.  [**ServerNotify**](iorpcdebugnotify-servernotify.md):1084FA00-9674-101A-B07B-00DD01113F11
    5.  [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md):22080240-9674-101A-B07B-00DD01113F11
    6.  [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md):2FC09500-9674-101A-B07B-00DD01113F11
-   Cuatro bytes siguientes: reservados para uso futuro.

> [!Note]
>
> Usado por todos los métodos de [**la interfaz IOrpcDebugNotify.**](iorpcdebugnotify.md)

 

</dd> <dt>

**pMessage**
</dt> <dd>

Puntero a una [**estructura RPCOLEMESSAGE**](/windows/win32/api/objidlbase/ns-objidlbase-rpcolemessage) que contiene información de serialización de datos RPC.

> [!Note]
>
> Usado por los [**métodos ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)y [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**refiid**
</dt> <dd>

Puntero al IID de la [**interfaz IOrpcDebugNotify.**](iorpcdebugnotify.md)

> [!Note]
>
> Usado por los [**métodos ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md), [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)y [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**pChannel**
</dt> <dd>

Puntero a la [**interfaz IRpcChannelBuffer**](/windows/win32/api/objidlbase/nn-objidlbase-irpcchannelbuffer) de la implementación del canal RPC COM en el servidor.

> [!Note]
>
> Usado por los [**métodos ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)y [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**pUnkProxyMgr**
</dt> <dd>

Puntero a la [**interfaz IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) del objeto implicado en esta invocación del depurador. Puede ser **NULL;** sin embargo, esto reduce la funcionalidad del depurador.

> [!Note]
>
> Usado por los [**métodos ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md)y [**ClientNotify.**](iorpcdebugnotify-clientnotify.md)

 

</dd> <dt>

**pInterface**
</dt> <dd>

Puntero a la interfaz COM del método que invocará este RPC. No debe ser **NULL.**

> [!Note]
>
> Usado por los [**métodos ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)y [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**pUnkObject**
</dt> <dd>

Debe ser **NULL.**

> [!Note]
>
> Usado por los [**métodos ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md), [**ServerGetBufferSize**](iorpcdebugnotify-servergetbuffersize.md)y [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**Hresult**
</dt> <dd>

El propósito de este miembro cambia para cada una de las notificaciones siguientes:

[**ClientGetBufferSize:**](iorpcdebugnotify-clientgetbuffersize.md)el número de bytes que el depurador de cliente transmitirá al depurador del servidor. Si es cero, no es necesario transmitir ninguna información.

[**ClientNotify:**](iorpcdebugnotify-clientnotify.md) **el HRESULT** de la última RPC.

[**ServerGetBufferSize:**](iorpcdebugnotify-servergetbuffersize.md)el número de bytes que el depurador de cliente transmitirá al depurador del servidor. Si es cero, no es necesario transmitir ninguna información.

> [!Note]
>
> Usado por los [**métodos ClientGetBufferSize**](iorpcdebugnotify-clientgetbuffersize.md), [**ClientNotify**](iorpcdebugnotify-clientnotify.md)y [**ServerGetBufferSize.**](iorpcdebugnotify-servergetbuffersize.md)

 

</dd> <dt>

**pvBuffer**
</dt> <dd>

Puntero a una estructura [**BUFFER \_ de DBG \_ DE ORPC**](orpc-dbg-buffer.md) que contiene la información de depuración con referencia RPC. Es indefinido si **cbBuffer** es cero.

> [!Note]
>
> Usado por los [**métodos ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify,**](iorpcdebugnotify-clientnotify.md) [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)y [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**cbBuffer**
</dt> <dd>

Longitud, en bytes, de los datos a los que apunta **pvBuffer**.

> [!Note]
>
> Usado por los [**métodos ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientNotify,**](iorpcdebugnotify-clientnotify.md) [**ServerFillBuffer**](iorpcdebugnotify-serverfillbuffer.md)y [**ServerNotify.**](iorpcdebugnotify-servernotify.md)

 

</dd> <dt>

**lpcbBuffer**
</dt> <dd>

Número de bytes que el depurador de cliente transmitirá al depurador del servidor. Si es cero, no es necesario transmitir ninguna información. Este valor reemplaza al valor devuelto en **hresult**.

> [!Note]
>
> Usado por los [**métodos ClientFillBuffer**](iorpcdebugnotify-clientfillbuffer.md), [**ClientGetBufferSize.**](iorpcdebugnotify-clientgetbuffersize.md)

 

</dd> <dt>

**reserved**
</dt> <dd>

Reservado. No utilizar.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                     |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                           |
| Encabezado<br/>                   | <dl> <dt>N/D</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**BÚFER \_ DE DBG DE ORPC \_**](orpc-dbg-buffer.md)
</dt> <dt>

[**ARGUMENTOS \_ DE ORPC INIT \_**](orpc-init-args.md)
</dt> <dt>

[**DllDebugObjectRPCHook**](dlldebugobjectrpchook.md)
</dt> <dt>

[**IOrpcDebugNotify**](iorpcdebugnotify.md)
</dt> </dl>

 

