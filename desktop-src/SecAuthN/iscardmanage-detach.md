---
description: Libera los datos adjuntos a una tarjeta inteligente o un lector determinados asignados por AttachByHandle y AttachByIFD, respectivamente.
ms.assetid: 601b35a6-9094-4786-b94c-5cd1283feef5
title: MÉTODO ISCardManage::D etach
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Detach
api_type:
- COM
api_location: ''
ms.openlocfilehash: 067c8e9f3e8cee607281d5f0a80ca813e91b425e63c15d3c1d47661acbbd04d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014095"
---
# <a name="iscardmanagedetach-method"></a>MÉTODO ISCardManage::D etach

\[El **método Detach** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método Detach** libera los datos adjuntos a una tarjeta [*inteligente*](../secgloss/s-gly.md) o un lector determinados asignados por [](../secgloss/r-gly.md) [**AttachByHandle**](iscardmanage-attachbyhandle.md) y [**AttachByIFD,**](iscardmanage-attachbyifd.md) respectivamente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Detach();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles:



| Código devuelto                                                                                   | Descripción                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                    |



 

## <a name="remarks"></a>Comentarios

Para adjuntar una llamada de tarjeta [**inteligente, llame a AttachByHandle**](iscardmanage-attachbyhandle.md) [**o AttachByIFD.**](iscardmanage-attachbyifd.md)

Para volver a conectarse con la tarjeta inteligente sin llamar **a Detach** y [**AttachByHandle,**](iscardmanage-attachbyhandle.md)llame a [**Volver a conectar**](iscardmanage-reconnect.md).

Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardManage**](iscardmanage.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AttachByHandle**](iscardmanage-attachbyhandle.md)
</dt> <dt>

[**AttachByIFD**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**Volver a conectar**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
