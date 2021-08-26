---
description: Convierte una matriz de bytes típica de C/C++ en un búfer universal de bytes (objeto IStream).
ms.assetid: 512c561a-63f1-463e-9bae-9bec1ebdbe9b
title: Método ISCardTypeConv::ConvertByteArrayToByteBuffer (Scarddat.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardTypeConv.ConvertByteArrayToByteBuffer
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 5616dc56ac893d6298e12014f3ee31d38bf1c55fb5367f354bf97da704ade0c6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013815"
---
# <a name="iscardtypeconvconvertbytearraytobytebuffer-method"></a>Método ISCardTypeConv::ConvertByteArrayToByteBuffer

\[El **método ConvertByteArrayToByteBuffer** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. Los [módulos de tarjeta inteligente](/previous-versions/windows/desktop/secsmart/smart-card-modules) proporcionan una funcionalidad similar.\]

El **método ConvertByteArrayToByteBuffer** convierte una matriz de bytes típica de C/C++ en un búfer universal de bytes **(objeto IStream).**

El búfer de bytes creado es una secuencia asignada a través de un bloque de memoria. Para acceder al búfer o administrarlo, use los métodos proporcionados por la **interfaz IStream.** Una característica única sobre esta implementación de matriz es que cuando se llama al método **IStream::Release,** se liberará la memoria subyacente.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ConvertByteArrayToByteBuffer(
  [in]  LPBYTE       pbyArray,
  [in]  DWORD        dwArraySize,
  [out] LPBYTEBUFFER *ppbyBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pbyArray* \[ En\]
</dt> <dd>

Puntero a la matriz de bytes que se va a convertir.

</dd> <dt>

*dwArraySize* \[ En\]
</dt> <dd>

Tamaño de la matriz de bytes que se va a convertir.

</dd> <dt>

*ppbyBuffer* \[ out\]
</dt> <dd>

Puntero al **objeto IStream** que se va a devolver.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve uno de los siguientes valores posibles:



| Código devuelto                                                                                   | Descripción                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Memoria asignada correctamente.<br/>                                                        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | Hay algún problema con uno o varios de los parámetros pasados a la función.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | Un parámetro de tipo de puntero era incorrecto.<br/>                                            |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay suficiente memoria libre para satisfacer la solicitud.<br/>                                            |



 

## <a name="remarks"></a>Comentarios

La memoria asignada es móvil. Use el **método IStream::Release** para liberar la memoria.

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

 

 
