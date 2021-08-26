---
description: Determina el tamaño, en bytes, de la interfaz COM IStream.
ms.assetid: 8c2f081d-cc41-409e-a868-bcf834e1f128
title: Método ISCardTypeConv::SizeOfIStream (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.SizeOfIStream
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ec150fdf5a6f296b5728131cd59bb6863016fe46fe0769e6159e43b236f77a95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013695"
---
# <a name="iscardtypeconvsizeofistream-method"></a>Método ISCardTypeConv::SizeOfIStream

\[El **método SizeOfIStream** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método SizeOfIStream** determina el tamaño, en bytes, de la interfaz COM **de IStream.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SizeOfIStream(
  [in]  LPSTREAM       pStrm,
  [out] ULARGE_INTEGER *puliSize
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pStrm* \[ En\]
</dt> <dd>

Puntero a la interfaz COM **de IStream.**

</dd> <dt>

*puliSize* \[ out\]
</dt> <dd>

Puntero al entero grande sin signo que puede contener todo el valor sizeof de 64 bits de la interfaz COM **IStream.**

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles.



| Código devuelto                                                                                  | Descripción                                                                                             |
|----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | La función se ha hecho *\* correctamente y puliSize* es el tamaño, en bytes, de la interfaz COM de IStream.<br/> |
| <dl> <dt>**E \_ FAIL**</dt> </dl>       | Error no especificado.<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | El *parámetro puliSize* es incorrecto.<br/>                                                       |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>    | El *parámetro pStrm* es incorrecto.<br/>                                                          |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | Se ha producido un error inesperado.<br/>                                                                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scarddat.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scarddat.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID ISCardTypeConv se define como \_ 53B6AA63-3F56-11D0-916B-00AA00C18068<br/>       |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ISCardTypeConv**](iscardtypeconv.md)
</dt> <dt>

[Valores devueltos de tarjeta inteligente](authentication-return-values.md)
</dt> </dl>

 

 
