---
description: 'Método CTransInPlaceInputPin.NotifyAllocator: el método NotifyAllocator especifica un asignador para la conexión. Este método implementa el método IMemInputPin::NotifyAllocator.'
ms.assetid: adc1c5b6-99da-4140-b644-7b98f6b8bad4
title: Método CTransInPlaceInputPin.NotifyAllocator (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2397ea32d9069352207eba6a4a5b9709b1c7514fa7d2c5acd16a9539090dba3e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999215"
---
# <a name="ctransinplaceinputpinnotifyallocator-method"></a>CTransInPlaceInputPin.NotifyAllocator (método)

El `NotifyAllocator` método especifica un asignador para la conexión. Este método implementa el [**método IMemInputPin::NotifyAllocator.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAllocator* 
</dt> <dd>

Puntero a la interfaz [**IMemAllocator del asignador.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)

</dd> <dt>

*bReadOnly* 
</dt> <dd>

Marca que especifica si los ejemplos de este asignador son de solo lectura. Si **es TRUE,** los ejemplos son de solo lectura.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                               | Descripción                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Correcto<br/>                   |
| <dl> <dt>**E \_ FAIL**</dt> </dl>    | Error<br/>                   |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | **Argumento de** puntero NULL<br/> |



 

## <a name="remarks"></a>Comentarios

El filtro intenta usar el mismo asignador para ambas conexiones de pin.

-   Si el pin de salida no está conectado, el pin de entrada acepta automáticamente el asignador. Cuando el pin de salida está conectado, el filtro volverá a conectar el pin de entrada. En ese momento, el filtro volverá a intentar usar un solo asignador.
-   Si el pin de salida está conectado, el pin de entrada acepta el asignador. El pin de salida también usa el mismo asignador. Llama a `NotifyAllocator` en el pin de entrada de bajada.

El caso anterior tiene la siguiente excepción:

-   Si el asignador propuesto es de solo lectura (es decir, el parámetro *bReadOnly* es **TRUE)** y el filtro necesita modificar los ejemplos, el filtro debe usar dos asignadores diferentes. En este caso, si el filtro ascendente está proponiendo usar el asignador del filtro de bajada, el método devuelve E \_ FAIL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransInPlaceInputPin (clase)**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




