---
description: La función AttachPropertyInstanceEx asigna una propiedad existente a una ubicación específica de los datos reconocidos y modifica el valor de los datos de la propiedad.
ms.assetid: 08bd1959-5ce8-4cb8-af8b-abbf4839c484
title: Función AttachPropertyInstanceEx (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachPropertyInstanceEx
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 1e0841c49e54d10d38a56d6206bc255b0aa7c49a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677741"
---
# <a name="attachpropertyinstanceex-function"></a>AttachPropertyInstanceEx función)

La función **AttachPropertyInstanceEx** asigna una propiedad existente a una ubicación específica de los datos reconocidos y modifica el valor de los datos de la propiedad.

## <a name="syntax"></a>Sintaxis


```C++
BOOL WINAPI AttachPropertyInstanceEx(
  _In_ HFRAME    hFrame,
  _In_ HPROPERTY hProperty,
  _In_ DWORD     Length,
  _In_ ULPVOID   lpData,
  _In_ DWORD     LengthEx,
  _In_ ULPVOID   lpDataEx,
  _In_ DWORD     HelpID,
  _In_ DWORD     IndentLevel,
  _In_ DWORD     IFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ de\]
</dt> <dd>

Identificador del marco que se está analizando. Use el identificador que se pasa a la DLL del analizador en el parámetro *hFrame* de la función [**AttachProperties**](attachproperties.md) .

</dd> <dt>

*hProperty* \[ de\]
</dt> <dd>

Identificador de una estructura [**PROPERTYINFO**](propertyinfo.md) que define la propiedad. Cuando se implementa la función de exportación de [**registro**](register-parser.md) , se especifica la estructura **PROPERTYINFO** que define la propiedad.

</dd> <dt>

*Longitud* \[ de\]
</dt> <dd>

Longitud de los datos para esta instancia de la propiedad.

</dd> <dt>

*lpData* \[ de\]
</dt> <dd>

Puntero a la ubicación de los datos reconocidos donde se encuentra el valor de propiedad. Use el puntero que se pasa a la DLL del analizador en el parámetro *lpProtocol* de la función [**AttachProperties**](attachproperties.md) .

</dd> <dt>

*LengthEx* \[ de\]
</dt> <dd>

Longitud de la longitud de los datos extendidos en bytes.

</dd> <dt>

*lpDataEx* \[ de\]
</dt> <dd>

Puntero a los datos extendidos, que suele ser una variable de pila que contiene los datos de extensión.

</dd> <dt>

*HelpID* \[ de\]
</dt> <dd>

Identificador (de 0 a 2047) que se usa para establecer la ayuda contextual de una propiedad.

El número *helpID* es relativo al archivo de ayuda asociado a la [*base de datos de propiedades*](p.md)de protocolo.

</dd> <dt>

*IndentLevel* \[ de\]
</dt> <dd>

Nivel de sangría (de 0 a 15) que se usa para mostrar una propiedad jerárquicamente.

Monitor de red usa los niveles de 0 a 9. El nivel 15 es un valor especial que permite al analizador adjuntar una propiedad oculta que no está visible.

</dd> <dt>

*IFlags* \[ de\]
</dt> <dd>

Un valor de campo de bits que indica el orden de los BITs dentro de una propiedad. Los analizadores anteriores que establecen *fError* en 0 o 1 ahora deberían establecer *fError* en IFLAG \_ error. Establezca este parámetro en uno de los siguientes valores.



| Value                                                                                                                                                         | Significado                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <dt>**\_error IFLAG**</dt> </dl>       | Los datos del marco tienen un error.<br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <dt>**IFLAG \_ intercambiada**</dt> </dl> | En el momento de la asociación, **Word** byte es un formato que no es de Intel.<br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <dt>**IFLAG \_ UNIcode**</dt> </dl> | En el momento de la asociación, la **cadena** es Unicode.<br/>               |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es **true**.

Si la función no se realiza correctamente, el valor devuelto es **false**.

## <a name="remarks"></a>Observaciones

Se llama a la función **AttachPropertyInstanceEx** durante la implementación de la función de exportación [**AttachProperties**](attachproperties.md) . Cuando se adjunta una propiedad a los datos mediante AttachPropertyInstanceEx, Monitor de red crea una estructura [**PROPERTYINST**](propertyinst.md) que define la instancia de la propiedad adjunta y una estructura [**PROPERTYINSTEX**](propertyinstex.md) que define los datos extendidos.

Si se llama a **AttachPropertyInstanceEx** y no se proporcionan datos extendidos, el parámetro *lpDataEx* es **null** o el parámetro *LengthEx* es 0, la llamada **AttachPropertyInstanceEx** es funcionalmente equivalente a una llamada [**AttachPropertyInstance**](attachpropertyinstance.md) .

Durante la implementación de [**AttachProperties**](attachproperties.md), llame a [**AttachPropertyInstance**](attachpropertyinstance.md) para usar los datos tal como existen en la captura. También puede llamar a la función **AttachPropertyInstanceEx** para modificar los datos de la propiedad. Sin embargo, se recomienda que use los datos tal como existen en la captura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon. h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




