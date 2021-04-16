---
description: Crea un vínculo de comunicación a un lector, utilizando un nombre para mostrar proporcionado para el lector.
ms.assetid: 7916896b-c460-47b2-a1db-17d8fc9bdd2e
title: 'ISCardManage:: AttachByIFD (método)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByIFD
api_type:
- COM
api_location: ''
ms.openlocfilehash: ae0aaae2157331d5d1bae2814c563c89dc73c757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648457"
---
# <a name="iscardmanageattachbyifd-method"></a>ISCardManage:: AttachByIFD (método)

\[El método **AttachByIFD** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El método **AttachByIFD** crea un vínculo de comunicación a un [*lector*](../secgloss/r-gly.md), utilizando un nombre para mostrar proporcionado para el lector.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT AttachByIFD(
  [in] BSTR bstrIFDName
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrIFDName* \[ de\]
</dt> <dd>

Nombre para mostrar del lector.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles:



| Código devuelto                                                                                   | Descripción                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Operación completada correctamente.<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El parámetro *bstrIFDName* no es válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/>                            |



 

## <a name="remarks"></a>Observaciones

Para adjuntar una llamada de [*tarjeta inteligente*](../secgloss/s-gly.md) [**AttachByHandle**](iscardmanage-attachbyhandle.md).

Para liberar la [**desasociación**](iscardmanage-detach.md)de una llamada de datos adjuntos.

Para volver a conectar con la tarjeta inteligente sin llamar a [**detach**](iscardmanage-detach.md) y **AttachByIFD**, llame a [**reconnect**](iscardmanage-reconnect.md).

Para obtener una lista de todos los métodos definidos por esta interfaz, vea [**ISCardManage**](iscardmanage.md).

Además de los códigos de error COM enumerados anteriormente, esta interfaz puede devolver un código de error de tarjeta inteligente si se llamó a una función de tarjeta inteligente para completar la solicitud. Para obtener más información, vea [valores devueltos de tarjeta inteligente](authentication-return-values.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>          |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/> |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AttachByHandle**](iscardmanage-attachbyhandle.md)
</dt> <dt>

[**Conecta**](iscardmanage-detach.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**Volver a conectar**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
