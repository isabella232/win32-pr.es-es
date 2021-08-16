---
description: El tipo de enumeración WPD PARAMETER USAGE TYPES describe cómo se usa un \_ parámetro de método en un método \_ \_ determinado.
ms.assetid: 60cbb4fa-c5fd-4402-bfd4-8fd95c009a33
title: WPD_PARAMETER_USAGE_TYPES enumeración (PortableDevice.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_PARAMETER_USAGE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 8ece49d1b961ce6ce5c14241d14bf69480e1eb79028f57a2cb959f5d7c4b79dc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117842081"
---
# <a name="wpd_parameter_usage_types-enumeration"></a>Enumeración \_ WPD PARAMETER \_ USAGE \_ TYPES

El [**tipo de \_ enumeración WPD PARAMETER \_ USAGE \_ TYPES**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types) describe cómo se usa un parámetro de método en un método determinado.

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWPD_PARAMETER_USAGE_TYPES { 
  WPD_PARAMETER_USAGE_RETURN  = 0,
  WPD_PARAMETER_USAGE_IN      = 1,
  WPD_PARAMETER_USAGE_OUT     = 2,
  WPD_PARAMETER_USAGE_INOUT   = 3
} WPD_PARAMETER_USAGE_TYPES;
```



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**WPD \_ PARAMETER \_ USAGE \_ RETURN**
</dt> <dd>

El parámetro recibe el valor devuelto, si lo especifica el método .

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**USO DE \_ PARÁMETROS \_ WPD \_ EN**
</dt> <dd>

El parámetro contiene un valor de entrada antes de llamar al método .

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**USO DE \_ PARÁMETROS \_ WPD \_ OUT**
</dt> <dd>

El parámetro contiene un valor de salida cuando el método devuelve .

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**ENTRADA DE \_ USO DE PARÁMETROS DE \_ \_ WPD**
</dt> <dd>

El parámetro contiene un valor de entrada antes de llamar al método y un valor de salida cuando se devuelve.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



 

