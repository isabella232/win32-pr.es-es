---
description: 'El método Revert descarta todos los cambios realizados en una secuencia de transacción desde la última llamada a IByteBuffer:: commit.'
ms.assetid: da3d9810-6511-43d5-af87-03a392f8be75
title: 'Método IByteBuffer:: revert (Scardssp. h)'
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
ms.openlocfilehash: cf7873407196c98868ca45c73db503568f8259e0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275336"
---
# <a name="ibytebufferrevert-method"></a>IByteBuffer:: revert (método)

\[El método **Revert** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]

El método **Revert** descarta todos los cambios realizados en una secuencia de transacción desde la última llamada a [**IByteBuffer:: commit**](ibytebuffer-commit.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Revert();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **HRESULT**. Un valor de S \_ correcto indica que la llamada se realizó correctamente y que la secuencia se revirtió a su versión anterior.

## <a name="remarks"></a>Observaciones

Este método descarta los cambios realizados en una secuencia de transacción desde la última operación de confirmación.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra la reversión de un flujo de transacción a la última operación confirmada.


```C++
HRESULT  hr;

hr = pIByteBuff->Revert();
if (FAILED(hr))
  printf("Failed IByteBuffer::Revert\n");
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

