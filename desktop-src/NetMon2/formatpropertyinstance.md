---
description: Da formato a los datos de instancia de la propiedad mediante el formateador genérico que proporciona Monitor de red.
ms.assetid: 36206601-7519-45c8-a14e-707b318c539d
title: Función FormatPropertyInstance (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FormatPropertyInstance
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 39d51df93a04efa8631fcfbd583075d7e3500bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677293"
---
# <a name="formatpropertyinstance-function"></a>FormatPropertyInstance función)

La función **FormatPropertyInstance** da formato a los datos de instancia de la propiedad mediante el formateador genérico que proporciona monitor de red.

## <a name="syntax"></a>Sintaxis


```C++
DWORD WINAPIV FormatPropertyInstance(
  _Inout_ LPPROPERTYINST lpPropertyInst
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*lpPropertyInst* \[ in, out\]
</dt> <dd>

Puntero a una estructura [PROPERTYINST](propertyinst.md) que contiene los datos de instancia.

En la entrada, el formateador genérico toma los datos de la instancia de uno de los miembros de la Unión **PROPERTYINST** y convierte los datos en una cadena con formato predefinida.

En la salida, el formateador genérico establece el miembro **szPropertyText** de la estructura **PROPERTYINST** en un puntero a la cadena con formato.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ Success.

Si la función no es correcta, el valor devuelto es un código de error de NMerr. h.

## <a name="remarks"></a>Observaciones

El archivo DLL del analizador llama indirectamente a la función **FormatPropertyInstance** cuando se requiere el formateador genérico para dar formato a los datos para su presentación en el panel de detalles de la interfaz de usuario de monitor de red. Para llamar a **FormatPropertyInstance** , especifíquelo en el miembro **InstanceData** de la estructura [PROPERTYINFO](propertyinfo.md) al definir la propiedad.

> [!Note]  
> El analizador no reconoce la función a la que se llama cuando debe dar formato a una instancia de una propiedad. La función puede ser **FormatPropertyInstance** o una función de formato personalizado definida por el analizador. El analizador llama a la función de formato especificada por el miembro **InstanceData** de la estructura **PROPERTYINFO** para la propiedad.

 

Para obtener más información y un ejemplo de cómo implementar [formatproperties](formatproperties.md), vea [implementar formatproperties](implementing-formatproperties.md). Para obtener más información sobre cómo el formateador genérico da formato a distintos tipos de datos, vea la [salida del formateador genérico](generic-formatter-output.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[PROPERTYINFO](propertyinfo.md)
</dt> <dt>

[PROPERTYINST](propertyinst.md)
</dt> </dl>

 

 




