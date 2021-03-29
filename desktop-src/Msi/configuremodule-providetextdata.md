---
description: Mergemod.dll llama al método ProvideTextData para recuperar datos de texto de la herramienta cliente. Mergemod.dll proporciona el nombre de la entrada correspondiente en la tabla ModuleConfiguration.
ms.assetid: 286b0b58-1b6a-4d41-89e1-eb9c23bdd788
title: Método ConfigureModule. ProvideTextData (Mergemod. h)
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
ms.openlocfilehash: 6801cb4b3ff90cb277d13573fe4527e8d76bfe0d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653921"
---
# <a name="configuremoduleprovidetextdata-method"></a>ConfigureModule. ProvideTextData, método

Mergemod.dll llama al método **ProvideTextData** para recuperar datos de texto de la herramienta cliente. Mergemod.dll proporciona el *nombre* de la entrada correspondiente en la tabla ModuleConfiguration.

La herramienta debe devolver S \_ correcto y proporcionar el texto de personalización adecuado en ConfigData. La herramienta cliente es responsable de la asignación de los datos, pero Mergemod.dlles responsable de liberar la memoria. Este argumento debe ser un objeto **BSTR** . **LPCWSTR** no se acepta.

Si la herramienta no proporciona ningún dato de configuración para este valor de *nombre* , la función debe devolver S \_ false. En este caso Mergemod.dll omite el valor del argumento ConfigData y usa el valor predeterminado de la tabla ModuleConfiguration.

Cualquier código de retorno distinto de S \_ OK o s \_ false producirá un error que se registrará (si hay un registro abierto) y dará lugar a errores de combinación.

Dado que esta función sigue la Convención **BSTR** estándar, NULL es equivalente a la cadena vacía.

## <a name="syntax"></a>Sintaxis


```JScript
ConfigureModule.ProvideTextData(
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

Consulte [**función ProvideTextData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 2,0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod. h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




