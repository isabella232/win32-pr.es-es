---
title: Método IReferenceClock Unadvise
description: El método Unadvise cancela una solicitud de notificación.
ms.assetid: 9817a054-0c6c-402f-afb1-54748ff46a4b
keywords:
- Formato multimedia de windows del método Unadvise
- Método Unadvise windows Media Format , IReferenceClock (interfaz)
- IReferenceClock interface windows Media Format , Método Unadvise
topic_type:
- apiref
api_name:
- IReferenceClock.Unadvise
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: ba093eefcedb48f2fb46a55ad8a90f9715c6e3c9
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127256299"
---
# <a name="ireferenceclockunadvise-method"></a>IReferenceClock::Unadvise (método)

El **método Unadvise** cancela una solicitud de notificación.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Unadvise(
   DWORD dwAdviseCookie
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dwAdviseCookie* 
</dt> <dd>

Identificador de la solicitud que se quitará. Use el valor devuelto por AdviseTime en el parámetro pdwAdviseCookie.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un valor **HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                             | Descripción                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>    | El método se ha llevado a cabo de forma correcta.<br/>                    |
| <dl> <dt>**S \_ FALSE**</dt> </dl> | El identificador pasado no existe.<br/> |



 

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IReferenceClock (interfaz)**](ireferenceclock.md)
</dt> </dl>

 

 





