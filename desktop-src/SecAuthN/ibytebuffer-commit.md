---
description: El método Commit garantiza que los cambios realizados en un objeto abierto en modo de transacción se reflejan en el almacenamiento primario.
ms.assetid: 00986e48-c5b9-4ac9-a204-a0774cb5e03e
title: Método IByteBuffer::Commit (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Commit
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 066925361d0ee4391bcd1eaafe33e0ae2d4b9120
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259727"
---
# <a name="ibytebuffercommit-method"></a>IByteBuffer::Commit (método)

\[El **método Commit** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La [**interfaz IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]

El **método Commit** garantiza que los cambios realizados en un objeto abierto en modo de transacción se reflejan en el almacenamiento primario.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Commit(
  [in] LONG grfCommitFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*grfCommitFlags* \[ En\]
</dt> <dd>

Controla la forma en que se confirman los cambios realizados en un objeto de secuencia. Para obtener una definición de estos valores, vea la enumeración STGC.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **un HRESULT.** Un valor de S \_ OK indica que la llamada se ha realizado correctamente.

## <a name="remarks"></a>Observaciones

Este método garantiza que los cambios en un objeto de secuencia abierto en modo de transacción se reflejan en el almacenamiento primario. Los cambios realizados en la secuencia desde que se abrió o se confirmaron por última vez se reflejan en el objeto de almacenamiento primario. Si el elemento primario se abre en modo de transacción, es posible que el elemento primario revierta posteriormente los cambios en este objeto de secuencia. La implementación de archivo compuesto no admite la apertura de secuencias en modo de transacción, por lo que este método tiene muy poco efecto que vaciar búferes de memoria.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo confirmar los cambios en el almacenamiento.


```C++
HRESULT  hr;

// Commit the buffer.
hr = pIByteBuff->Commit(STGC_DEFAULT | STGC_CONSOLIDATE);
if (FAILED(hr))
  printf("Failed IByteBuffer::Commit\n");
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows XP \[ solo aplicaciones de escritorio\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

