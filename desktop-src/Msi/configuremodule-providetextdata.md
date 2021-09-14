---
description: El método ProvideTextData es llamado por Mergemod.dll para recuperar datos de texto de la herramienta cliente. Mergemod.dll proporciona el nombre de la entrada correspondiente en la tabla ModuleConfiguration.
ms.assetid: 286b0b58-1b6a-4d41-89e1-eb9c23bdd788
title: Método ConfigureModule.ProvideTextData (Mergemod.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158786"
---
# <a name="configuremoduleprovidetextdata-method"></a>Método ConfigureModule.ProvideTextData

El **método ProvideTextData** es llamado por Mergemod.dll para recuperar datos de texto de la herramienta cliente. Mergemod.dll proporciona el *nombre de* la entrada correspondiente en la tabla ModuleConfiguration.

La herramienta debe devolver S \_ OK y proporcionar el texto de personalización adecuado en ConfigData. La herramienta cliente es responsable de asignar los datos, pero Mergemod.dll es responsable de liberar la memoria. Este argumento DEBE ser un **objeto BSTR.** **LPCWSTR** NO se acepta.

Si la herramienta no proporciona ningún dato de configuración para este *valor name,* la función debe devolver S \_ FALSE. En este caso, Mergemod.dll omite el valor del argumento ConfigData y usa el valor Predeterminado de la tabla ModuleConfiguration.

Cualquier código de retorno que no sea S OK o S FALSE hará que se registre un error (si un registro está abierto) y producirá un error \_ \_ en la combinación.

Dado que esta función sigue la convención **estándar de BSTR,** null es equivalente a la cadena vacía.

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

No se puede llamar al cliente más de una vez por cada registro de la [tabla ModuleConfiguration](moduleconfiguration-table.md). Tenga en cuenta Mergemod.dll realiza varias llamadas al cliente para el mismo valor de "Nombre". Si ningún registro de la tabla ModuleSubstitution usa la propiedad , una entrada de la tabla ModuleConfiguration no produce ninguna llamada al cliente.

### <a name="c"></a>C++

Vea [**Función ProvideTextData**](/windows/desktop/api/Mergemod/nf-mergemod-imsmconfiguremodule-providetextdata).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|-----------------------------------------------------------------------------------------|
| Versión<br/> | Mergemod.dll 2.0 o posterior<br/>                                                    |
| Encabezado<br/>  | <dl> <dt>Mergemod.h</dt> </dl>   |
| Archivo DLL<br/>     | <dl> <dt>Mergemod.dll</dt> </dl> |



 

 




