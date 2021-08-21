---
title: XTYP_MONITOR transacción (Ddeml.h)
description: La datos dinámicos Exchange de devolución de llamada DDE de un depurador de datos dinámicos Exchange (DDE), DdeCallback, recibe la transacción monitor de XTYP cada vez que se produce un evento DDE en \_ el sistema.
ms.assetid: a27791b1-c1b4-4516-b050-71da164fa80a
keywords:
- XTYP_MONITOR datos de transacción Exchange
topic_type:
- apiref
api_name:
- XTYP_MONITOR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 11a86235c2964bbd09d51ce3adc2e602e23fed09597df14721e92e76c0cd8109
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119047263"
---
# <a name="xtyp_monitor-transaction"></a>Transacción monitor de XTYP \_

La datos dinámicos Exchange de devolución de llamada DDE de un depurador de datos dinámicos Exchange (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe la transacción monitor de **\_ XTYP** cada vez que se produce un evento DDE en el sistema. Para recibir esta transacción, una aplicación debe especificar el valor **\_ MONITOR de APPCLASS** cuando llama a la [**función DdeInitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_MONITOR            (0x00F0 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK)
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

No se usa.

</dd> <dt>

*hsz2* 
</dt> <dd>

No se usa.

</dd> <dt>

*hdata* 
</dt> <dd>

Identificador de un objeto DDE que contiene información sobre el evento DDE. La aplicación debe usar la [**función DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata) para obtener un puntero al objeto .

</dd> <dt>

*dwData1* 
</dt> <dd>

No se usa.

</dd> <dt>

*dwData2* 
</dt> <dd>

Evento DDE. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                                      | Significado                                                                                                                                                                                                                                                                                                                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MF_CALLBACKS"></span><span id="mf_callbacks"></span><dl> <dt>**MF \_ Devoluciones de llamada**</dt> <dt>0x08000000</dt> </dl> | El sistema envió una transacción a una función de devolución de llamada DDE. El objeto DDE contiene una [**estructura MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct) que proporciona información sobre la transacción.<br/>                                                                                                                                               |
| <span id="MF_CONV"></span><span id="mf_conv"></span><dl> <dt>**MF \_ Conv**</dt> <dt>0x40000000</dt> </dl>                | Se estableció o finalizó una conversación de DDE. El objeto DDE contiene una [**estructura MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct) que proporciona información sobre la conversación.<br/>                                                                                                                                                  |
| <span id="MF_ERRORS"></span><span id="mf_errors"></span><dl> <dt>**MF \_ ERRORES**</dt> <dt>0x10000000</dt> </dl>          | Se produjo un error DDE. El objeto DDE contiene una [**estructura MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct) que proporciona información sobre el error.<br/>                                                                                                                                                                                       |
| <span id="MF_HSZ_INFO"></span><span id="mf_hsz_info"></span><dl> <dt>**MF \_ HSZ \_ INFO**</dt> <dt>0x01000000</dt> </dl>   | Una aplicación DDE creó, libera o incrementó el recuento de uso de un identificador de cadena, o bien se libera un identificador de cadena como resultado de una llamada a la función [**DdeUninitialize.**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize) El objeto DDE contiene una [**estructura MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa) que proporciona información sobre el identificador de cadena.<br/> |
| <span id="MF_LINKS"></span><span id="mf_links"></span><dl> <dt>**MF \_ Vínculos**</dt> <dt>0x20000000</dt> </dl>             | Una aplicación DDE inició o detuvo un bucle de aviso. El objeto DDE contiene una [**estructura MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct) que proporciona información sobre el bucle advise.<br/>                                                                                                                                                |
| <span id="MF_POSTMSGS"></span><span id="mf_postmsgs"></span><dl> <dt>**MF \_ 0x04000000 POSTMSGS**</dt> <dt></dt> </dl>    | El sistema o una aplicación publicaron un mensaje DDE. El objeto DDE contiene una [**estructura MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) que proporciona información sobre el mensaje.<br/>                                                                                                                                                        |
| <span id="MF_SENDMSGS"></span><span id="mf_sendmsgs"></span><dl> <dt>**MF \_ SendMSGS**</dt> <dt>0x02000000</dt> </dl>    | El sistema o una aplicación enviaron un mensaje DDE. El objeto DDE contiene una [**estructura MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct) que proporciona información sobre el mensaje.<br/>                                                                                                                                                          |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función de devolución de llamada procesa esta transacción, debe devolver 0.

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

[**DdeAccessData**](/windows/desktop/api/Ddeml/nf-ddeml-ddeaccessdata)
</dt> <dt>

[**DdeInitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeinitializea)
</dt> <dt>

[**DdeUninitialize**](/windows/desktop/api/Ddeml/nf-ddeml-ddeuninitialize)
</dt> <dt>

[**MONCBSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-moncbstruct)
</dt> <dt>

[**MONCONVSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monconvstruct)
</dt> <dt>

[**MONERRSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monerrstruct)
</dt> <dt>

[**MONHSZSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monhszstructa)
</dt> <dt>

[**MONLINKSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monlinkstruct)
</dt> <dt>

[**MONMSGSTRUCT**](/windows/win32/api/ddeml/ns-ddeml-monmsgstruct)
</dt> <dt>

**Conceptual**
</dt> <dt>

[datos dinámicos Exchange management library](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

