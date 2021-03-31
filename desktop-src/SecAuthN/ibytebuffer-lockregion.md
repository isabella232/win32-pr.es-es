---
description: Restringe el acceso a un intervalo de bytes especificado en el objeto de búfer.
ms.assetid: 7bcb3c1e-5739-41f7-a3aa-2943542943ed
title: 'IByteBuffer:: LockRegion (método) (Scardssp. h)'
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
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278582"
---
# <a name="ibytebufferlockregion-method"></a>IByteBuffer:: LockRegion (método)

\[El método **LockRegion** está disponible para su uso en los sistemas operativos especificados en la sección de requisitos. No está disponible para su uso en Windows Server 2003 con Service Pack 1 (SP1) y versiones posteriores, Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La interfaz [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) proporciona una funcionalidad similar.\]

El método **LockRegion** restringe el acceso a un intervalo de bytes especificado en el objeto de búfer.

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

*libOffset* \[ de\]
</dt> <dd>

Entero que especifica el desplazamiento de bytes para el principio del intervalo.

</dd> <dt>

*CB* \[ de\]
</dt> <dd>

Entero que especifica la longitud del intervalo, en bytes, que se va a restringir.

</dd> <dt>

*dwLockType* \[ de\]
</dt> <dd>

Especifica las restricciones que se solicitan al tener acceso al intervalo. Puede ser uno de los valores de la tabla siguiente.



| Value                                                                                                                                                            | Significado                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="LOCK_WRITE"></span><span id="lock_write"></span><dl> <dt>**escritura de BLOQUEos \_**</dt> </dl>             | El intervalo especificado de bytes se puede abrir y leer cualquier número de veces, pero la escritura en el intervalo bloqueado está prohibida, excepto para el propietario que concedió este bloqueo.<br/>                                                                      |
| <span id="LOCK_EXCLUSIVE"></span><span id="lock_exclusive"></span><dl> <dt>**BLOQUEO \_ exclusivo**</dt> </dl> | La escritura en el intervalo de bytes especificado está prohibida, excepto para el propietario al que se concedió este bloqueo.<br/>                                                                                                                                       |
| <span id="LOCK_ONLYONCE"></span><span id="lock_onlyonce"></span><dl> <dt>**BLOQUEAR \_ ONLYONCE**</dt> </dl>    | Si se concede este bloqueo, no \_ se puede obtener ningún otro bloqueo de ONLYONCE de bloqueo en el intervalo. Normalmente, este tipo de bloqueo es un alias para algún otro tipo de bloqueo. Por lo tanto, las implementaciones específicas pueden tener un comportamiento adicional asociado a este tipo de bloqueo.<br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El valor devuelto es **HRESULT**. Un valor de S \_ correcto indica que la llamada se realizó correctamente.

## <a name="remarks"></a>Observaciones

El intervalo de bytes puede extenderse más allá del final actual de la secuencia. El bloqueo más allá del final de una secuencia es útil como método de comunicación entre las distintas instancias de la secuencia sin cambiar los datos que realmente forman parte de la secuencia.

Se admiten tres tipos de bloqueo: el bloqueo para excluir otros escritores, el bloqueo para excluir otros lectores o escritores, y el bloqueo que permite a un solo solicitante obtener un bloqueo en el intervalo determinado, que suele ser un alias de uno de los otros dos tipos de bloqueo. Una instancia de Stream determinada podría admitir cualquiera de los dos primeros tipos, o ambos. El tipo de bloqueo se especifica mediante *dwLockType*, con un valor de la enumeración [**LOCKTYPE**](/windows/win32/api/objidl/ne-objidl-locktype) .

Posteriormente, cualquier región bloqueada con **LockRegion** debe desbloquearse explícitamente llamando a [**IByteBuffer:: UnlockRegion**](ibytebuffer-unlockregion.md) con exactamente los mismos valores para los parámetros *libOffset*, *CB* y *dwLockType* . La región debe desbloquearse antes de que se libere la secuencia. Dos regiones adyacentes no se pueden bloquear por separado y, a continuación, desbloquearse con una sola llamada de desbloqueo.

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
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows XP \[\]<br/>                                             |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                    |
| Fin de compatibilidad de cliente<br/>    | Windows XP<br/>                                                                   |
| Fin de compatibilidad de servidor<br/>    | Windows Server 2003<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Scardssp. h</dt> </dl>   |
| Biblioteca de tipos<br/>             | <dl> <dt>Scardssp. tlb</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ IByteBuffer se define como E126F8FE-A7AF-11D0-B88A-00C04FD424B9<br/>          |



 

