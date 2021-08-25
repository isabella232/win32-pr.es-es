---
description: La función AttachPropertyInstanceEx asigna una propiedad existente a una ubicación específica de los datos reconocidos y modifica el valor de los datos de propiedad.
ms.assetid: 08bd1959-5ce8-4cb8-af8b-abbf4839c484
title: Función AttachPropertyInstanceEx (Netmon.h)
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
ms.openlocfilehash: e184ec0b874d55d149c9d049b8c6b2cafd716fe82c66410e2d3e1550b397c366
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119911285"
---
# <a name="attachpropertyinstanceex-function"></a>Función AttachPropertyInstanceEx

La **función AttachPropertyInstanceEx** asigna una propiedad existente a una ubicación específica de los datos reconocidos y modifica el valor de los datos de propiedad.

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

*hFrame* \[ En\]
</dt> <dd>

Controle el marco que se está analizando. Use el identificador pasado al archivo DLL del analizador en el *parámetro hFrame* de la [**función AttachProperties.**](attachproperties.md)

</dd> <dt>

*hProperty* \[ En\]
</dt> <dd>

Identificador de una [**estructura PROPERTYINFO**](propertyinfo.md) que define la propiedad . Al implementar la función [**register**](register-parser.md) export, especifique la **estructura PROPERTYINFO** que define la propiedad .

</dd> <dt>

*Longitud* \[ En\]
</dt> <dd>

Longitud de los datos de esta instancia de la propiedad .

</dd> <dt>

*lpData* \[ En\]
</dt> <dd>

Puntero a la ubicación de los datos reconocidos donde se encuentra el valor de propiedad. Use el puntero pasado al archivo DLL del analizador en el *parámetro lpProtocol* de la [**función AttachProperties.**](attachproperties.md)

</dd> <dt>

*LengthEx* \[ En\]
</dt> <dd>

Longitud de la longitud de datos extendida en bytes.

</dd> <dt>

*lpDataEx* \[ En\]
</dt> <dd>

Puntero a los datos extendidos, que normalmente es una variable de pila que contiene los datos de extensión.

</dd> <dt>

*HelpID* \[ En\]
</dt> <dd>

Identificador (de 0 a 2047) que se usa para establecer la Ayuda contextual para una propiedad.

El *número helpID* es relativo al archivo de Ayuda asociado a la base de datos de [*propiedades de protocolo*](p.md).

</dd> <dt>

*IndentLevel* \[ En\]
</dt> <dd>

Nivel de sangría (de 0 a 15) utilizado para mostrar una propiedad jerárquicamente.

Monitor de red usa los niveles 0 a 9. El nivel 15 es un valor especial que permite al analizador adjuntar una propiedad oculta que no está visible.

</dd> <dt>

*IFlags* \[ En\]
</dt> <dd>

Valor de campo BIT que indica el orden de los BIT dentro de una propiedad. Los analizadores anteriores que *establecen fError* en 0 o 1 ahora deben establecer *fError* en IFLAG \_ ERROR. Establezca este parámetro en uno de los valores siguientes.



| Value                                                                                                                                                         | Significado                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <span id="IFLAG_ERROR"></span><span id="iflag_error"></span><dl> <dt>**ERROR DE IFLAG \_**</dt> </dl>       | Los datos del marco tienen un error.<br/>                      |
| <span id="IFLAG_SWAPPED"></span><span id="iflag_swapped"></span><dl> <dt>**IFLAG \_ SWAPPED**</dt> </dl> | En el momento de la **asociación,** el byte WORD es un formato que no es Intel.<br/> |
| <span id="IFLAG_UNICODE"></span><span id="iflag_unicode"></span><dl> <dt>**IFLAG \_ UNICODE**</dt> </dl> | En el momento de la asociación, **STRING** es Unicode.<br/>               |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función se realiza correctamente, el valor devuelto es **TRUE.**

Si la función no se realiza correctamente, el valor devuelto es **FALSE.**

## <a name="remarks"></a>Comentarios

Se **llama a la función AttachPropertyInstanceEx** durante la implementación de la función de exportación [**AttachProperties.**](attachproperties.md) Cuando una propiedad se adjunta a los datos mediante AttachPropertyInstanceEx, Monitor de red crea una estructura [**PROPERTYINST**](propertyinst.md) que define la instancia de la propiedad adjunta y una [**estructura PROPERTYINSTEX**](propertyinstex.md) que define los datos extendidos.

Si se llama **a AttachPropertyInstanceEx** y no se proporcionan datos extendidos, el parámetro *lpDataEx* es **NULL** o el parámetro *LengthEx* es 0, la llamada **AttachPropertyInstanceEx** es funcionalmente equivalente a una [**llamada AttachPropertyInstance.**](attachpropertyinstance.md)

Durante la implementación de [**AttachProperties,**](attachproperties.md)llame [**a AttachPropertyInstance**](attachpropertyinstance.md) para usar los datos tal como existen en la captura. También puede llamar a la **función AttachPropertyInstanceEx** para modificar los datos de propiedad. Sin embargo, se recomienda usar los datos tal como existen en la captura.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                           |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl>  |
| Biblioteca<br/>                  | <dl> <dt>Nmapi.lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Nmapi.dll</dt> </dl> |



 

 




