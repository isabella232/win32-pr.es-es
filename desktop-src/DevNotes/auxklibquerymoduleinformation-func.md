---
description: Recupera información sobre el conjunto de módulos cargado actualmente para el sistema.
ms.assetid: d3dc57e3-2c42-46cb-9af0-5f06bff60ad9
title: Función AuxKlibQueryModuleInformation (Aux \_ klib.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AuxKlibQueryModuleInformation
api_type:
- LibDef
api_location:
- Aux_klib.lib
ms.openlocfilehash: be734583c8b7d02be4c498bc75069a0c813565d48aea3db3826712d6375e72b4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045325"
---
# <a name="auxklibquerymoduleinformation-function"></a>Función AuxKlibQueryModuleInformation

Recupera información sobre el conjunto de módulos cargado actualmente para el sistema.

## <a name="syntax"></a>Sintaxis


```C++
NTSTATUS _stdcall AuxKlibQueryModuleInformation(
  _Inout_   PULONG BufferSize,
  _In_      ULONG  ElementSize,
  _Out_opt_ PVOID  QueryInfo
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*BufferSize* \[ in, out\]
</dt> <dd>

En la entrada, el tamaño del búfer *QueryInfo,* en bytes. En la salida, recibe el tamaño real necesario. Dado que la lista de módulos del sistema puede cambiar entre llamadas, este valor también puede cambiar entre llamadas.

</dd> <dt>

*ElementSize* \[ En\]
</dt> <dd>

Tamaño, en bytes, de un elemento de matriz. Este tamaño determina el formato de la salida.

</dd> <dt>

*QueryInfo* \[ out, opcional\]
</dt> <dd>

Puntero a un búfer que recibe la información del módulo. Esta información se devuelve en una matriz cuyos elementos son una de las estructuras siguientes: [**AUX \_ MODULE BASIC \_ \_ INFO**](aux-module-basic-info-struct.md) o [**AUX MODULE EXTENDED \_ \_ \_ INFO**](aux-module-extended-info-struct.md). La estructura específica usada depende del tamaño de elemento especificado.

Si este parámetro es **NULL,** la función devuelve el tamaño de búfer necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es STATUS \_ SUCCESS.

Si se produce un error en la función, el valor devuelto puede ser uno de los códigos de estado definidos en Ntstatus.h, que está disponible en WDK.

## <a name="remarks"></a>Comentarios

Debe llamar a la [**función AuxKlibInitialize antes**](auxklibinitialize-func.md) de llamar a esta función.

La biblioteca de objetos que implementa esta API se puede descargar desde [aquí.](https://www.microsoft.com/?ref=go)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|------------------------------------------------------------------------------------------|
| Redistribuible<br/> | Windows Biblioteca de API auxiliar versión 1.0 o posterior<br/>                            |
| Header<br/>          | <dl> <dt>Auxiliar \_ klib.h</dt> </dl>   |
| Biblioteca<br/>         | <dl> <dt>Auxiliar \_ klib.lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AuxKlibInitialize**](auxklibinitialize-func.md)
</dt> <dt>

[**INFORMACIÓN \_ BÁSICA DEL MÓDULO \_ \_ AUXILIAR**](aux-module-basic-info-struct.md)
</dt> <dt>

[**INFORMACIÓN \_ AMPLIADA DEL MÓDULO \_ \_ AUXILIAR**](aux-module-extended-info-struct.md)
</dt> </dl>

 

 




