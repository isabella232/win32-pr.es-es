---
description: El mensaje CREATEDIALOGINSTANCE de la línea \_ de TSPI hace que TAPI cree una asociación entre el proveedor de servicios y una instancia de la función providerGenericDialog de TUISPI que se \_ ejecuta en el contexto de la aplicación.
ms.assetid: 5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75
title: Mensaje de LINE_CREATEDIALOGINSTANCE (TSPI. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c92088b79bdd085874d14817e6e9652f03c6c00
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680180"
---
# <a name="line_createdialoginstance-message"></a>Mensaje de línea \_ CREATEDIALOGINSTANCE

El mensaje **\_ CREATEDIALOGINSTANCE** de la línea de TSPI hace que TAPI cree una asociación entre el proveedor de servicios y una instancia de la función [**\_ providerGenericDialog de TUISPI**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) que se ejecuta en el contexto de la aplicación que invocó la función TSPI asincrónica identificada por el parámetro *dwRequestID* de la estructura [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) a la que apunta *lpTUISPICreateDialogInstanceParams*.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProvider* 
</dt> <dd>

ProviderHandle que se proporciona al proveedor de servicios como parámetro de [**TSPI \_ providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices).

</dd> <dt>

*lpTUISPICreateDialogInstanceParams* 
</dt> <dd>

Puntero a una estructura [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) .

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2,0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>TSPI. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TSPI \_ providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)
</dt> <dt>

[**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
</dt> </dl>

 

