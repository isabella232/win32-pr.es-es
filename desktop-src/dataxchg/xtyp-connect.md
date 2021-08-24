---
title: XTYP_CONNECT transacción (Ddeml.h)
description: Un cliente usa la transacción XTYP \_ CONNECT para establecer una conversación.
ms.assetid: 74f43b10-f7ac-4370-9caa-7b9ddf3413ed
keywords:
- XTYP_CONNECT datos de transacción Exchange
topic_type:
- apiref
api_name:
- XTYP_CONNECT
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1ff7a7a79d8b61deef6b5f19b829e5c8dd8f4603c5f60c3b47d0a84b0603736
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119793425"
---
# <a name="xtyp_connect-transaction"></a>Transacción XTYP \_ CONNECT

Un cliente usa la **transacción XTYP \_ CONNECT** para establecer una conversación. Una función de devolución de llamada de servidor de datos dinámicos Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe esta transacción cuando un cliente especifica un nombre de servicio que el servidor admite (y un nombre de tema que no es **NULL)** en una llamada a la función [**DdeConnect.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)


```C++
#define     XCLASS_BOOL              0x1000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_CONNECT            (0x0060 | XCLASS_BOOL | XTYPF_NOBLOCK)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*uType* 
</dt> <dd>

El tipo de transacción.

</dd> <dt>

*uFmt* 
</dt> <dd>

No se usa.

</dd> <dt>

*hconv* 
</dt> <dd>

No se usa.

</dd> <dt>

*hsz1* 
</dt> <dd>

Identificador del nombre del tema.

</dd> <dt>

*hsz2* 
</dt> <dd>

Identificador del nombre del servicio.

</dd> <dt>

*hdata* 
</dt> <dd>

No se usa.

</dd> <dt>

*dwData1* 
</dt> <dd>

Puntero a una [**estructura CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) que contiene información de contexto para la conversación. Si el cliente no es una aplicación DDEML, este parámetro es 0.

</dd> <dt>

*dwData2* 
</dt> <dd>

Especifica si el cliente es la misma instancia de aplicación que el servidor. Si el parámetro es 1, el cliente es la misma instancia. Si el parámetro es 0, el cliente es una instancia diferente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una función de devolución de llamada de servidor debe devolver **TRUE** para permitir que el cliente establezca una conversación en el nombre de servicio y el par de nombre de tema especificados, o bien la función debe devolver **FALSE** para denegar la conversación. Si la función de devolución de llamada devuelve **TRUE** y se establece correctamente una conversación, el sistema pasa el identificador de conversación al servidor mediante la emisión de una transacción [**XTYP \_ CONNECT \_ CONFIRM**](xtyp-connect-confirm.md) a la función de devolución de llamada del servidor (a menos que el servidor haya especificado la marca **CBF SKIP CONNECT \_ \_ \_ CONFIRMS** en la función [**DdeInitialize).**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

## <a name="remarks"></a>Comentarios

Esta transacción se filtra si la aplicación de servidor especificó la marca **CBF \_ FAIL \_ CONNECTIONS** en la [**función DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)

Un servidor no puede bloquear este tipo de transacción; Se omite el código de retorno **\_ CBR BLOCK.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Ddeml.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext)
</dt> <dt>

[**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

**Conceptual**
</dt> <dt>

[datos dinámicos Exchange management library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

