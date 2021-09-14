---
description: Restringe el acceso a un intervalo especificado de bytes en el objeto de búfer.
ms.assetid: 7bcb3c1e-5739-41f7-a3aa-2943542943ed
title: Método IByteBuffer::LockRegion (Scardssp.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IByteBuffer.LockRegion
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: ae227d11892b604ab1382cb328dc492e4596f278
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071302"
---
# <a name="ibytebufferlockregion-method"></a>IByteBuffer::LockRegion (método)

\[El **método LockRegion** está disponible para su uso en los sistemas operativos especificados en la sección Requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La [**interfaz IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]

El **método LockRegion** restringe el acceso a un intervalo especificado de bytes en el objeto de búfer.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT LockRegion(
  [in] LONG libOffset,
  [in] LONG cb,
  [in] LONG dwLockType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*libOffset* \[ En\]
</dt> <dd>

Entero que especifica el desplazamiento de bytes para el principio del intervalo.

</dd> <dt>

*cb* \[ En\]
</dt> <dd>

Entero que especifica la longitud del intervalo, en bytes, que se va a restringir.

</dd> <dt>

*dwLockType* \[ En\]
</dt> <dd>

Especifica las restricciones que se solicitan para acceder al intervalo. Puede ser uno de los valores de la tabla siguiente.



| Value                                                                                                                                                            | Significado                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOCK_WRITE"></span><span id="lock_write"></span><dl> <dt>**ESCRITURA DE \_ BLOQUEO**</dt> </dl>             | El intervalo de bytes especificado se puede abrir y leer varias veces, pero la escritura en el intervalo bloqueado está prohibida, excepto para el propietario al que se concedió este bloqueo.<br/>                                                                      |
| <span id="LOCK_EXCLUSIVE"></span><span id="lock_exclusive"></span><dl> <dt>**BLOQUEO \_ EXCLUSIVO**</dt> </dl> | La escritura en el intervalo de bytes especificado está prohibida, excepto para el propietario al que se concedió este bloqueo.<br/>                                                                                                                                       |
| <span id="LOCK_ONLYONCE"></span><span id="lock_onlyonce"></span><dl> <dt>**LOCK \_ ONLYONCE**</dt> </dl>    | Si se concede este bloqueo, no se puede obtener ningún otro bloqueo LOCK \_ ONLYONCE en el intervalo. Normalmente, este tipo de bloqueo es un alias para algún otro tipo de bloqueo. Por lo tanto, las implementaciones específicas pueden tener un comportamiento adicional asociado a este tipo de bloqueo.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **un HRESULT.** Un valor de S \_ OK indica que la llamada se ha realizado correctamente.

## <a name="remarks"></a>Observaciones

El intervalo de bytes puede extenderse más allá del final actual de la secuencia. El bloqueo más allá del final de una secuencia es útil como método de comunicación entre diferentes instancias de la secuencia sin cambiar los datos que realmente forman parte de la secuencia.

Se pueden admite tres tipos de bloqueo: bloqueo para excluir otros escritores, bloqueo para excluir otros lectores o escritores y bloqueo que permite que solo un solicitante obtenga un bloqueo en el intervalo especificado, que suele ser un alias para uno de los otros dos tipos de bloqueo. Una instancia de secuencia determinada puede admitir cualquiera de los dos primeros tipos, o ambos. *DwLockType* especifica el tipo de bloqueo mediante un valor de la [**enumeración LOCKTYPE.**](/windows/win32/api/objidl/ne-objidl-locktype)

Cualquier región bloqueada con **LockRegion** debe desbloquearse más adelante explícitamente llamando a [**IByteBuffer::UnlockRegion**](ibytebuffer-unlockregion.md) con exactamente los mismos valores para los parámetros *libOffset*, *cb* y *dwLockType.* La región debe desbloquearse antes de que se libera la secuencia. Dos regiones adyacentes no se pueden bloquear por separado y, a continuación, desbloquearse con una sola llamada de desbloqueo.

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra cómo restringir el acceso a un intervalo de bytes.


```C++
HRESULT  hr;

// Lock a region.
hr = pIByteBuff->LockRegion(0, 10, LOCK_EXCLUSIVE);
if (FAILED(hr))
  printf("Failed IByteBuffer::LockRegion\n");
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



 

