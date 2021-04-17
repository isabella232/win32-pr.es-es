---
description: Recupera información sobre el conjunto de módulos cargados actualmente para el sistema.
ms.assetid: d3dc57e3-2c42-46cb-9af0-5f06bff60ad9
title: Función AuxKlibQueryModuleInformation (AUX \_ klib. h)
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
ms.openlocfilehash: 00649b042e13ecbc055a132d1de5c5c3248ba0e7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660266"
---
# <a name="auxklibquerymoduleinformation-function"></a>AuxKlibQueryModuleInformation función)

Recupera información sobre el conjunto de módulos cargados actualmente para el sistema.

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

En la entrada, el tamaño del búfer *QueryInfo* , en bytes. En la salida, recibe el tamaño necesario real. Dado que la lista de módulos del sistema puede cambiar entre llamadas, este valor también puede cambiar entre llamadas.

</dd> <dt>

*Elementos de elemento* \[ de\]
</dt> <dd>

Tamaño, en bytes, de un elemento de la matriz. Este tamaño determina el formato de la salida.

</dd> <dt>

*QueryInfo* \[ out, opcional\]
</dt> <dd>

Un puntero a un búfer que recibe la información del módulo. Esta información se devuelve en una matriz cuyos elementos son una de las siguientes estructuras: [**\_ \_ \_ información básica del módulo AUX**](aux-module-basic-info-struct.md) o [**\_ \_ \_ información ampliada del módulo AUX**](aux-module-extended-info-struct.md). La estructura específica que se utiliza depende del tamaño del elemento especificado.

Si este parámetro es **null**, la función devuelve el tamaño de búfer necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se ejecuta correctamente, el valor devuelto es STATUs \_ Success.

Si se produce un error en la función, el valor devuelto puede ser uno de los códigos de estado definidos en NTSTATUS. h, que está disponible en el WDK.

## <a name="remarks"></a>Observaciones

Debe llamar a la función [**AuxKlibInitialize**](auxklibinitialize-func.md) antes de llamar a esta función.

La biblioteca de objetos que implementa esta API se puede descargar desde [aquí](https://www.microsoft.com/?ref=go).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|----------------------------|------------------------------------------------------------------------------------------|
| Redistribuible<br/> | Biblioteca de API auxiliar de Windows versión 1,0 o posterior<br/>                            |
| Encabezado<br/>          | <dl> <dt>AUX \_ klib. h</dt> </dl>   |
| Biblioteca<br/>         | <dl> <dt>AUX \_ klib. lib</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**AuxKlibInitialize**](auxklibinitialize-func.md)
</dt> <dt>

[**\_ \_ información básica del módulo AUX \_**](aux-module-basic-info-struct.md)
</dt> <dt>

[**\_ \_ información adicional del módulo AUX \_**](aux-module-extended-info-struct.md)
</dt> </dl>

 

 




