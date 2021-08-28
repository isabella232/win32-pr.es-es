---
title: XTYP_ERROR transacción (Ddeml.h)
description: Una datos dinámicos Exchange de devolución de llamada (DDE), DdeCallback, recibe la transacción ERROR de XTYP \_ cuando se produce un error crítico.
ms.assetid: 710daa04-ed83-42e3-a55e-6ccf891a3d52
keywords:
- XTYP_ERROR datos de transacción Exchange
topic_type:
- apiref
api_name:
- XTYP_ERROR
api_location:
- Ddeml.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce59800723758201b4857b5a3ae0844675347b2d4fd403c77650b36d9275bfb6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119755985"
---
# <a name="xtyp_error-transaction"></a>Transacción XTYP \_ ERROR

Una datos dinámicos Exchange de devolución de llamada (DDE), [*DdeCallback*](/windows/win32/api/ddeml/nc-ddeml-pfncallback), recibe la transacción ERROR de **\_ XTYP** cuando se produce un error crítico.


```C++
#define     XCLASS_NOTIFICATION      0x8000
#define     XTYPF_NOBLOCK            0x0002
#define     XTYP_ERROR              (0x0000 | XCLASS_NOTIFICATION | XTYPF_NOBLOCK )
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

Identificador de la conversación asociada al error. Este parámetro es **NULL** si el error no está asociado a una conversación.

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

No se usa.

</dd> <dt>

*dwData1* 
</dt> <dd>

Código de error en la palabra de orden bajo. Actualmente, solo se admite el código de error siguiente.



| Value                                                                                                                                                                      | Significado                                                                                      |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------|
| <span id="DMLERR_LOW_MEMORY"></span><span id="dmlerr_low_memory"></span><dl> <dt>**MEMORIA BAJA DE DMLERR \_ \_**</dt> </dl> | La memoria es baja; es posible que se pierdan datos de asesoramiento, de ejecución o de ejecución, o bien que se pueda producir un error en el sistema.<br/> |



 

</dd> <dt>

*dwData2* 
</dt> <dd>

No se usa.

</dd> </dl>

## <a name="remarks"></a>Comentarios

Una aplicación no puede bloquear este tipo de transacción; Se omite el código de retorno **\_ CBR BLOCK.** La datos dinámicos Exchange management library (DDEML) intenta liberar memoria mediante la eliminación de recursos no críticos. Una aplicación que haya bloqueado las conversaciones debe desbloquearlas.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                             |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                   |
| Encabezado<br/>                   | <dl> <dt>Ddeml.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[datos dinámicos Exchange información general de la biblioteca de administración de recursos](dynamic-data-exchange-management-library.md)
</dt> </dl>

 

