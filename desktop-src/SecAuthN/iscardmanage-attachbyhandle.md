---
description: Crea un vínculo de comunicación a una tarjeta inteligente (ICC) mediante un identificador devuelto por el administrador de recursos de tarjeta inteligente.
ms.assetid: dfd05dce-4416-4881-92ca-c85baccf3b86
title: Método ISCardManage::AttachByHandle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByHandle
api_type:
- COM
api_location: ''
ms.openlocfilehash: 266b6a0d2a4027fe85f1f5539b970a44fc21bbee
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127244220"
---
# <a name="iscardmanageattachbyhandle-method"></a>Método ISCardManage::AttachByHandle

\[El **método AttachByHandle** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método AttachByHandle** crea un vínculo de comunicación a una [*tarjeta inteligente*](../secgloss/s-gly.md) (ICC) mediante un identificador devuelto por el administrador de recursos de tarjeta [*inteligente.*](../secgloss/r-gly.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AttachByHandle(
  [in] HSCARD hICC
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hICC* \[ En\]
</dt> <dd>

Identificador de una tarjeta inteligente.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles:



| Código devuelto                                                                                   | Descripción                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Operación completada correctamente.<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro hICC* no es válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                     |



 

## <a name="remarks"></a>Observaciones

Para adjuntar una [*llamada de lector,*](../secgloss/r-gly.md) [**llame a AttachByIFD.**](iscardmanage-attachbyifd.md)

Para liberar una llamada de datos [**adjuntos, llame a Detach**](iscardmanage-detach.md).

Para volver a conectarse con la tarjeta inteligente sin llamar [**a Detach**](iscardmanage-detach.md) y **AttachByHandle,** llame a [**Reconnect**](iscardmanage-reconnect.md).

Para obtener una lista de todos los métodos definidos por la [**interfaz ISCardManage,**](iscardmanage.md) vea [**ISCardManage**](iscardmanage.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener información sobre los códigos de error de tarjeta inteligente, vea [Valores devueltos de tarjeta inteligente.](authentication-return-values.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>          |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AttachByIFD**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**Separar**](iscardmanage-detach.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**Volver a conectar**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
