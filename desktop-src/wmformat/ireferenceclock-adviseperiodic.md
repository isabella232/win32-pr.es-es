---
title: Método IReferenceClock AdvisePeriodic
description: Este método no se implementa.
ms.assetid: b34ef914-992e-4ce2-943b-8bc36687a88a
keywords:
- AdvisePeriodic method windows Media Format
- Método AdvisePeriodic windows Media Format , interfaz IReferenceClock
- IReferenceClock interface windows Media Format , AdvisePeriodic (método)
topic_type:
- apiref
api_name:
- IReferenceClock.AdvisePeriodic
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 65b4020c42430d10e48125fa7d5f1481e7f0ee7c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127572192"
---
# <a name="ireferenceclockadviseperiodic-method"></a>IReferenceClock::AdvisePeriodic (método)

Este método no se implementa.

En otras implementaciones de la interfaz **IReferenceClock,** como en el componente DirectShow® de Microsoft® DirectX®, el método **AdvisePeriodic** se usa para crear una solicitud de aviso periódica que señalaría el objeto de evento especificado cada vez que transcurra el intervalo de tiempo especificado. Este SDK no implementa la funcionalidad de este método y las llamadas realizadas a él darán como resultado un valor devuelto de E \_ NOTIMPL.

## <a name="syntax"></a>Sintaxis


```C++
 AdvisePeriodic();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IReferenceClock (interfaz)**](ireferenceclock.md)
</dt> </dl>

 

 




