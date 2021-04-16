---
description: Mergemod.dll llama al método ProvideIntegerData del objeto ConfigureModule para recuperar datos enteros de la herramienta cliente.
ms.assetid: 13d48301-bd63-432c-b663-85a840886dda
title: Método ConfigureModule. ProvideIntegerData (Mergemod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ConfigureModule
- IMsmConfigureModule
api_type:
- COM
api_location:
- Mergemod.dll
ms.openlocfilehash: 482e1010dea850506b159b129eb4dcef77829fca
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671609"
---
# <a name="configuremoduleprovideintegerdata-method"></a>ConfigureModule. ProvideIntegerData, método

Mergemod.dll llama al método **ProvideIntegerData** del [**objeto ConfigureModule**](configuremodule-object.md) para recuperar datos enteros de la herramienta cliente.

Mergemod.dll proporciona el *nombre* de la entrada correspondiente en la [tabla ModuleConfiguration](moduleconfiguration-table.md).

La herramienta debe devolver S \_ correcto y proporcionar el entero de personalización correspondiente en *ConfigData*.

Si la herramienta no proporciona ningún dato de configuración para este valor de *nombre* , la función debe devolver S \_ false. En este caso Mergemod.dll omite el valor del argumento *ConfigData* y usa el valor predeterminado de la tabla ModuleConfiguration.

## <a name="syntax"></a>Sintaxis


```JScript
ConfigureModule.ProvideIntegerData(
  Name,
  ConfigData
)
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Nombre* 
</dt> <dd>

Nombre del elemento para el que se recuperan los datos.

</dd> <dt>

*ConfigData* 
</dt> <dd>

Puntero al texto de personalización.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Es posible que el cliente no se llame más de una vez para cada registro de la [tabla ModuleConfiguration](moduleconfiguration-table.md). Tenga en cuenta que Mergemod.dll nunca realiza varias llamadas al cliente para el mismo valor "Name". Si no hay ningún registro en la tabla ModuleSubstitution que usa la propiedad, una entrada de la tabla ModuleConfiguration no hace ninguna llamada al cliente.

### <a name="c"></a>C++

Consulte [**función ProvideIntegerData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 2,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




