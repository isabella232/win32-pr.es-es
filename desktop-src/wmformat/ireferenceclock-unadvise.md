---
title: IReferenceClock unaconseje (método)
description: El método Unadvise cancela una solicitud de notificación.
ms.assetid: 9817a054-0c6c-402f-afb1-54748ff46a4b
keywords:
- Método unaconsej Windows Media Format
- Método unvise formato de Windows Media, interfaz IReferenceClock
- Interfaz IReferenceClock formato de Windows Media, método unvise
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
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104148956"
---
# <a name="ireferenceclockunadvise-method"></a>IReferenceClock:: Unadvise (método)

El método **Unadvise** cancela una solicitud de notificación.

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

Identificador de la solicitud que se va a quitar. Use el valor devuelto por AdviseTime en el parámetro pdwAdviseCookie.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

El método devuelve un **valor HRESULT**. Entre los valores posibles se incluyen los que se indican en la tabla siguiente, entre otros.



| Código devuelto                                                                             | Descripción                                         |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>    | El método se ha llevado a cabo de forma correcta.<br/>                    |
| <dl> <dt>**S \_ false**</dt> </dl> | El identificador pasado no existe.<br/> |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaz IReferenceClock**](ireferenceclock.md)
</dt> </dl>

 

 





