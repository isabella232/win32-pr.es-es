---
description: Quita la restricción de acceso en un intervalo de bytes previamente restringido mediante IByteBuffer::LockRegion.
ms.assetid: f2a1162e-7fc7-4a55-befb-0b017edb9fe2
title: Método IByteBuffer::UnlockRegion (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.UnlockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 798569621c1a46e73ea6fd8e2f4f3333c3a0cbcef32618797fcba39d35b55bf6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120127395"
---
# <a name="ibytebufferunlockregion-method"></a>IByteBuffer::UnlockRegion (método)

\[El **método UnlockRegion** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La [**interfaz IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]

El **método UnlockRegion** quita la restricción de acceso en un intervalo de bytes previamente restringido mediante [**IByteBuffer::LockRegion**](ibytebuffer-lockregion.md).

## <a name="syntax"></a>Sintaxis


```C++
HRESULT UnlockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*libOffset* \[ En\]
</dt> <dd>

Desplazamiento de bytes para el principio del intervalo.

</dd> <dt>

*cb* \[ En\]
</dt> <dd>

Longitud, en bytes, del intervalo que se va a restringir.

</dd> <dt>

*dwLockType* \[ En\]
</dt> <dd>

Restricciones de acceso previamente colocadas en el intervalo.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **un valor HRESULT.** Un valor de S \_ OK indica que la llamada se ha realizado correctamente.

## <a name="remarks"></a>Comentarios

El **método IByteBuffer::UnlockRegion** desbloquea una región bloqueada previamente mediante el [**método IByteBuffer::LockRegion.**](ibytebuffer-lockregion.md) Posteriormente, las regiones bloqueadas se deben desbloquear explícitamente llamando a **IByteBuffer::UnlockRegion** con exactamente los mismos valores para los parámetros *libOffset*, *cb* y *dwLockType.* La región debe desbloquearse antes de liberar la secuencia. Dos regiones adyacentes no se pueden bloquear por separado y, a continuación, desbloquearse con una sola llamada de desbloqueo.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo desbloquear un intervalo de bytes.


```C++
HRESULT  hr;

// Unlock a region.
hr = pIByteBuff->UnlockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::UnlockRegion\n");
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio XP\]<br/>                                             |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Header<br/>                   | <dl> <dt>Scardssp.h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp.tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

