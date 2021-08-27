---
description: El método Revert descarta todos los cambios realizados en una secuencia con transacciones desde la última llamada a IByteBuffer::Commit.
ms.assetid: da3d9810-6511-43d5-af87-03a392f8be75
title: Método IByteBuffer::Revert (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Revert
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 46e535560332c43d250b0a26183036342c8cca29144e3d2d1803582387af6bd8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101265"
---
# <a name="ibytebufferrevert-method"></a>IByteBuffer::Revert (método)

\[El **método Revert** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La [**interfaz IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]

El **método Revert** descarta todos los cambios realizados en una secuencia con transacciones desde la última llamada a [**IByteBuffer::Commit.**](ibytebuffer-commit.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Revert();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **un HRESULT**. Un valor de S OK indica que la llamada se ha realizado \_ correctamente y la secuencia se revirtó a su versión anterior.

## <a name="remarks"></a>Comentarios

Este método descarta los cambios realizados en una secuencia de transacción desde la última operación de confirmación.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo revertir una secuencia con transacciones a la última operación confirmada.


```C++
HRESULT  hr;

hr = pIByteBuff->Revert();
if (FAILED(hr))
  printf("Failed IByteBuffer::Revert\n");
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



 

