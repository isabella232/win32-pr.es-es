---
description: El método ProvideIntegerData del objeto ConfigureModule es llamado por Mergemod.dll para recuperar datos enteros de la herramienta cliente.
ms.assetid: 13d48301-bd63-432c-b663-85a840886dda
title: Método ConfigureModule.ProvideIntegerData (Mergemod.h)
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
ms.openlocfilehash: 96472a13902322d940dc7e756c3639f9befaf6764b3ede8521f27a885a50e8d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143696"
---
# <a name="configuremoduleprovideintegerdata-method"></a>Método ConfigureModule.ProvideIntegerData

El **método ProvideIntegerData** del [**objeto ConfigureModule**](configuremodule-object.md) es llamado por Mergemod.dll para recuperar datos enteros de la herramienta cliente.

Mergemod.dll proporciona el *nombre de* la entrada correspondiente en la [tabla ModuleConfiguration](moduleconfiguration-table.md).

La herramienta debe devolver S \_ OK y proporcionar el entero de personalización adecuado en *ConfigData*.

Si la herramienta no proporciona ningún dato de configuración para este *valor name,* la función debe devolver S \_ FALSE. En este caso Mergemod.dll omite el valor del *argumento ConfigData* y usa el valor Predeterminado de la tabla ModuleConfiguration.

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

## <a name="remarks"></a>Comentarios

No se puede llamar al cliente más de una vez por cada registro de la [tabla ModuleConfiguration](moduleconfiguration-table.md). Tenga en cuenta Mergemod.dll realiza varias llamadas al cliente para el mismo valor de "Nombre". Si ningún registro de la tabla ModuleSubstitution usa la propiedad , una entrada de la tabla ModuleConfiguration no produce ninguna llamada al cliente.

### <a name="c"></a>C++

Vea [**Función ProvideIntegerData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-provideintegerdata).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 2.0 o posterior<br/>                                                    |
| Header<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




