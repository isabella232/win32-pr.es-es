---
description: El método Initialize prepara el objeto IByteBuffer para su uso. Se debe llamar a este método antes de llamar a cualquier otro método de la interfaz IByteBuffer.
ms.assetid: 1b22e693-0add-4b80-a2c4-925ebd3ab3a6
title: Método IByteBuffer::Initialize (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Initialize
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 28a525b26d49dd5df8a2be3ba6a5af5a16459c26e191368badae34ca381488e6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119417635"
---
# <a name="ibytebufferinitialize-method"></a>IByteBuffer::Initialize (método)

\[El **método Initialize** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores. La [**interfaz IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]

El **método Initialize** prepara el objeto [**IByteBuffer**](ibytebuffer.md) para su uso. Se debe llamar a este método antes de llamar a cualquier otro método de la **interfaz IByteBuffer.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Initialize(
  [in] LONG lSize,
  [in] BYTE *pData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lSize* \[ En\]
</dt> <dd>

Tamaño inicial, en bytes, de los datos que va a contener la secuencia.

</dd> <dt>

*pData* \[ En\]
</dt> <dd>

Si no **es NULL,** los datos iniciales que se escribirán en la secuencia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **un HRESULT.** Un valor de S \_ OK indica que la llamada se ha realizado correctamente.

## <a name="remarks"></a>Observaciones

Al usar una nueva [**secuencia IByteBuffer,**](ibytebuffer.md) llame a este método antes de usar cualquiera de los otros **métodos IByteBuffer.**

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra la inicialización [**del objeto IByteBuffer.**](ibytebuffer.md)


```C++
UCHAR    ucFileName[] = {0x3f, 0x00};    // Master File (MF)
HRESULT  hr;

// pIByteRequest is a pointer to an instantiated IByteBuffer object.
hr = pIByteRequest->Initialize(2, ucFileName);
if (FAILED(hr))
    printf("Failed IByteBuffer::Initialize\n");
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

