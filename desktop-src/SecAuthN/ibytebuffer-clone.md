---
description: El método Clone crea un nuevo objeto con su propio puntero de búsqueda que hace referencia a los mismos bytes que el objeto IByteBuffer original.
ms.assetid: 41530f1d-81e5-4bea-a254-d7d741976904
title: 'IByteBuffer:: Clone (método) (Scardssp. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.Clone
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d994ef55665b03da2a7d657689682f893fdf071f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278140"
---
# <a name="ibytebufferclone-method"></a>IByteBuffer:: Clone (método)

\[El método **Clone** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]

El método **Clone** crea un nuevo objeto con su propio puntero de búsqueda que hace referencia a los mismos bytes que el objeto [**IByteBuffer**](ibytebuffer.md) original.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Clone(
  [out] LPBYTEBUFFER *ppByteBuffer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppByteBuffer* \[ enuncia\]
</dt> <dd>

Cuando se realiza correctamente, apunta a la ubicación de un puntero [**IByteBuffer**](ibytebuffer.md) al nuevo objeto de secuencia. Cuando haya terminado de usar el puntero **IByteBuffer** , suéltelo llamando a la función [**IUnknown:: Release**](/windows/win32/api/unknwn/nf-unknwn-iunknown-release) . Si se produce un error, este parámetro es **null**.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **HRESULT**. Un valor de S \_ correcto indica que la llamada se realizó correctamente.

## <a name="remarks"></a>Observaciones

Este método crea un nuevo objeto de secuencia para tener acceso a los mismos bytes, pero con un puntero de búsqueda independiente. El nuevo objeto de flujo ve los mismos datos que el objeto de flujo de origen. Los cambios que se escriben en un objeto son visibles inmediatamente en el otro. El bloqueo de intervalo se comparte entre los objetos de secuencia.

La configuración inicial del puntero de búsqueda en la instancia de la secuencia clonada es la misma que la configuración actual del puntero de búsqueda en la secuencia original en el momento de la operación de clonación.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra la clonación de la interfaz [**IByteBuffer**](ibytebuffer.md) .


```C++
HRESULT  hr;

// Clone the buffer.
hr = pIByteBuff->Clone(&pIByteClone);
if (FAILED(hr))
  printf("Failed IByteBuffer::Clone\n");
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



 

