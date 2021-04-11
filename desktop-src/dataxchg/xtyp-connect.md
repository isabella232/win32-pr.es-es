---
title: XTYP_CONNECT transacción (ddeml. h)
description: Un cliente usa la \_ transacción XTYP Connect para establecer una conversación.
ms.assetid: 74f43b10-f7ac-4370-9caa-7b9ddf3413ed
keywords:
- Intercambio de datos de transacciones XTYP_CONNECT
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
ms.openlocfilehash: e2268994f1be000373691d6c25dbb7220d3e109e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150418"
---
# <a name="xtyp_connect-transaction"></a>Transacción de conexión de XTYP \_

Un cliente usa la transacción **XTYP \_ Connect** para establecer una conversación. Una función de devolución de llamada de servidor Intercambio dinámico de datos (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe esta transacción cuando un cliente especifica un nombre de servicio que admite el servidor (y un nombre de tema que no es **null**) en una llamada a la función [**DdeConnect**](/windows/desktop/api/Ddeml/nf-ddeml-ddeconnect) .


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

No se utiliza.

</dd> <dt>

*hconv* 
</dt> <dd>

No se utiliza.

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

No se utiliza.

</dd> <dt>

*dwData1* 
</dt> <dd>

Puntero a una estructura [**CONVCONTEXT**](/windows/win32/api/ddeml/ns-ddeml-convcontext) que contiene información de contexto para la conversación. Si el cliente no es una aplicación DDEML, este parámetro es 0.

</dd> <dt>

*dwData2* 
</dt> <dd>

Especifica si el cliente es la misma instancia de aplicación que el servidor. Si el parámetro es 1, el cliente es la misma instancia. Si el parámetro es 0, el cliente es una instancia diferente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Una función de devolución de llamada de servidor debe devolver **true** para permitir que el cliente establezca una conversación en el nombre de servicio especificado y el par de nombre de tema, o la función debe devolver **false** para denegar la conversación. Si la función de devolución de llamada devuelve **true** y se establece una conversación correctamente, el sistema pasa el identificador de conversación al servidor mediante la emisión de una transacción de confirmación de conexión de XTYP a la función de devolución de llamada del servidor (a menos que el servidor haya especificado el marcador **CBF \_ SKIP \_ Connect \_** [**\_ \_ CONFIRM**](xtyp-connect-confirm.md) en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) ).

## <a name="remarks"></a>Observaciones

Esta transacción se filtra si la aplicación de servidor especificó la marca **CBF \_ FAIL \_ Connections** en la función [**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea) .

Un servidor no puede bloquear este tipo de transacción; se omite el código de retorno del **\_ bloque CBR** .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Ddeml. h (incluir Windows. h)</dt> </dl> |



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

**Vista**
</dt> <dt>

[Biblioteca de administración de Intercambio dinámico de datos](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

