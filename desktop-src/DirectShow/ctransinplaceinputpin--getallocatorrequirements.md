---
description: El método GetAllocatorRequirements recupera las propiedades del asignador solicitadas por el pin. Este método implementa el método IMemInputPin::GetAllocatorRequirements.
ms.assetid: 1355facc-f863-44b2-9284-8f06f62d39a2
title: Método CTransInPlaceInputPin.GetAllocatorRequirements (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a192ef973d59529dc7ced0a81591a998ac532e903201114d675f4d51bb59543
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119907265"
---
# <a name="ctransinplaceinputpingetallocatorrequirements-method"></a>Método CTransInPlaceInputPin.GetAllocatorRequirements

El `GetAllocatorRequirements` método recupera las propiedades del asignador solicitadas por el pin. Este método implementa el [**método IMemInputPin::GetAllocatorRequirements.**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-getallocatorrequirements)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pProps* 
</dt> <dd>

Puntero a una [**estructura ALLOCATOR \_ PROPERTIES,**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que se rellena con los requisitos.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Los valores posibles incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                               | Descripción                                                                                          |
|-------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | Correcto<br/>                                                                                   |
| <dl> <dt>**E \_ NOTIMPL**</dt> </dl> | El pin de salida no está conectado o el pin de entrada de bajada no admite el método .<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | **Argumento de** puntero NULL<br/>                                                                 |



 

## <a name="remarks"></a>Comentarios

Si el pin de salida está conectado, este método pasa la llamada al pin de entrada de bajada. De lo contrario, devuelve E \_ NOTIMPL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransInPlaceInputPin (clase)**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




