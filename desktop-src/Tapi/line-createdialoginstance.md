---
description: El mensaje CREATEDIALOGINSTANCE de TSPI LINE hace que TAPI cree una asociación entre el proveedor de servicios y una instancia de la función \_ TUISPI providerGenericDialog que se ejecuta en el contexto de la \_ aplicación.
ms.assetid: 5a7e34bc-1dc3-40c4-b07e-de5b88cbcd75
title: LINE_CREATEDIALOGINSTANCE mensaje (Tspi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c92088b79bdd085874d14817e6e9652f03c6c00
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250178"
---
# <a name="line_createdialoginstance-message"></a>Mensaje \_ LINE CREATEDIALOGINSTANCE

El mensaje **\_ CREATEDIALOGINSTANCE** de TSPI LINE hace que TAPI cree una asociación entre el proveedor de servicios y una instancia de la función [**TUISPI \_ providerGenericDialog**](/windows/win32/api/tspi/nf-tspi-tuispi_providergenericdialog) que se ejecuta en el contexto de la aplicación que invocó la función TSPI asincrónica identificada por el parámetro *dwRequestID* de la estructura [**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams) a la que apunta *lpTUISPICreateDialogInstanceParams*.


```C++
            
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hProvider* 
</dt> <dd>

ProviderHandle proporcionado al proveedor de servicios como parámetro para [**TSPI \_ providerEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices).

</dd> <dt>

*lpTUISPICreateDialogInstanceParams* 
</dt> <dd>

Puntero a una [**estructura TUISPICREATEDIALOGINSTANCEPARAMS.**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|-----------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 2.0 o posterior<br/>                                             |
| Encabezado<br/>       | <dl> <dt>Tspi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Proveedor \_ TSPIEnumDevices**](/windows/win32/api/tspi/nf-tspi-tspi_providerenumdevices)
</dt> <dt>

[**TUISPICREATEDIALOGINSTANCEPARAMS**](/windows/win32/api/tspi/ns-tspi-tuispicreatedialoginstanceparams)
</dt> </dl>

 

