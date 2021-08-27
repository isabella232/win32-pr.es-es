---
description: Recupera un puntero de interfaz e incrementa el recuento de referencias. Este método implementa el método INonDelegatingUnknown::NonDelegatingQueryInterface.
ms.assetid: 451ca350-f40b-4cbf-ac39-e86dadb48a24
title: Método CUnknown.NonDelegatingQueryInterface (Combase.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CUnknown.NonDelegatingQueryInterface
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 26e13d9d30c3da208bb702427ee99a9648a7f538ba0d5a6a1b359db41e2cd155
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120076015"
---
# <a name="cunknownnondelegatingqueryinterface-method"></a>Método CUnknown.NonDelegatingQueryInterface

Recupera un puntero de interfaz e incrementa el recuento de referencias. Este método implementa el **método INonDelegatingUnknown::NonDelegatingQueryInterface.**

## <a name="syntax"></a>Sintaxis


```C++
HRESULT NonDelegatingQueryInterface(
   REFIID riid,
   void   **ppv
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*riid* 
</dt> <dd>

Identificador de la interfaz.

</dd> <dt>

*Ppv* 
</dt> <dd>

Dirección de un puntero para recibir la interfaz.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                   | Descripción                                        |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | Correcto.<br/>                                |
| <dl> <dt>**E \_ NOINTERFACE**</dt> </dl> | El objeto no admite esta interfaz.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | **Argumento de** puntero NULL.<br/>              |



 

## <a name="remarks"></a>Comentarios

La **clase CUnknown** solo expone la **interfaz IUknown.** Invalide este método para exponer interfaces adicionales. Para obtener información sobre cómo invalidar este método, [vea How to Implement IUnknown](how-to-implement-iunknown.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Combase.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




