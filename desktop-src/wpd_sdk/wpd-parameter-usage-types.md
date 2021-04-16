---
description: El \_ tipo de \_ \_ enumeración de tipos de uso de parámetros de WPD describe cómo se utiliza un parámetro de método en un método determinado.
ms.assetid: 60cbb4fa-c5fd-4402-bfd4-8fd95c009a33
title: Enumeración WPD_PARAMETER_USAGE_TYPES (PortableDevice. h)
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
ms.openlocfilehash: 72d4ebffccc3d1bc7d446848c29ebbc60539430e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649695"
---
# <a name="wpd_parameter_usage_types-enumeration"></a>\_ \_ Enumeración de tipos de uso de parámetros de WPD \_

El tipo de enumeración de tipos de uso de parámetros de WPD describe cómo se utiliza un parámetro de método en un método determinado. [**\_ \_ \_**](/windows/desktop/wpd_sdk/wpd-parameter-usage-types)

## <a name="syntax"></a>Sintaxis


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

<span id="WPD_PARAMETER_USAGE_RETURN"></span><span id="wpd_parameter_usage_return"></span>**\_devolución del \_ uso del parámetro WPD \_**
</dt> <dd>

El parámetro recibe el valor devuelto, si lo especifica el método.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_IN"></span><span id="wpd_parameter_usage_in"></span>**\_ \_ uso de parámetros \_ de WPD en**
</dt> <dd>

El parámetro contiene un valor de entrada antes de que se llame al método.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_OUT"></span><span id="wpd_parameter_usage_out"></span>**uso de parámetros de WPD \_ \_ \_ fuera**
</dt> <dd>

El parámetro contiene un valor de salida cuando el método devuelve.

</dd> <dt>

<span id="WPD_PARAMETER_USAGE_INOUT"></span><span id="wpd_parameter_usage_inout"></span>**uso de parámetros de WPD \_ \_ \_ INOUT**
</dt> <dd>

El parámetro contiene un valor de entrada antes de que se llame al método y un valor de salida cuando devuelve.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



 

