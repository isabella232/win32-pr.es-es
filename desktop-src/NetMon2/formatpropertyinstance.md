---
description: Da formato a los datos de instancia de propiedad mediante el formateador genérico que Monitor de red proporciona.
ms.assetid: 36206601-7519-45c8-a14e-707b318c539d
title: Función FormatPropertyInstance (Netmon.h)
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
ms.openlocfilehash: 283cab8580e3c456a3d75727ab55f2f61dc623d91b593559aa0eb2ec07e4b26e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119890785"
---
# <a name="formatpropertyinstance-function"></a>Función FormatPropertyInstance

La **función FormatPropertyInstance** da formato a los datos de instancia de propiedad mediante el formateador genérico Monitor de red proporciona.

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

Puntero a una [estructura PROPERTYINST](propertyinst.md) que contiene los datos de instancia.

En la entrada, el formateador genérico toma los datos de instancia de uno de los miembros de unión **PROPERTYINST** y convierte los datos en una cadena con formato predefinida.

En la salida, el formateador genérico establece el **miembro szPropertyText** de la estructura **PROPERTYINST** en un puntero a la cadena con formato.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es NMERR \_ SUCCESS.

Si la función no se realiza correctamente, el valor devuelto es un código de error de NMerr.h.

## <a name="remarks"></a>Comentarios

El archivo DLL del analizador llama indirectamente a la función **FormatPropertyInstance** cuando el formateador genérico tiene que dar formato a los datos para mostrarse en el panel de detalles de la interfaz Monitor de red usuario. Para llamar **a FormatPropertyInstance,** es posible especificarlo en el **miembro InstanceData** de la [estructura PROPERTYINFO](propertyinfo.md) al definir la propiedad .

> [!Note]  
> El analizador no reconoce a qué función se llama cuando debe dar formato a una instancia de una propiedad. La función puede ser **FormatPropertyInstance** o una función de formato personalizado definida por el analizador. El analizador llama a cualquier función de formato especificada por el **miembro InstanceData** de la **estructura PROPERTYINFO** de la propiedad .

 

Para obtener más información y un ejemplo de cómo implementar [formatproperties](formatproperties.md), vea [Implementing FormatProperties](implementing-formatproperties.md). Para obtener más información sobre cómo el formateador genérico da formato a distintos tipos de datos, vea [Generic Formatter Output](generic-formatter-output.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propertyinfo](propertyinfo.md)
</dt> <dt>

[PROPERTYINST](propertyinst.md)
</dt> </dl>

 

 




