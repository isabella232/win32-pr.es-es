---
description: La función de exportación AttachProperties asigna las propiedades a una ubicación dentro de un fragmento de datos reconocidos. AttachProperties debe implementarse para cada analizador que admita el archivo DLL del analizador.
ms.assetid: ef28f571-8364-47d0-841c-580e89333afd
title: Función de devolución de llamada AttachProperties (Netmon.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AttachProperties
api_type:
- UserDefined
api_location:
- Netmon.h
ms.openlocfilehash: 018a54652ef5c24562a6c5220aa24da00276dce4729608cf59162bc11c7d7aee
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119012343"
---
# <a name="attachproperties-callback-function"></a>Función de devolución de llamada AttachProperties

La **función de exportación AttachProperties** asigna las propiedades a una ubicación dentro de un fragmento de datos reconocidos. **AttachProperties** debe implementarse para cada analizador que admita el archivo DLL del analizador.

## <a name="syntax"></a>Sintaxis


```C++
DWORD AttachProperties(
  _In_ HFRAME    hFrame,
  _In_ LPBYTE    lpFrame,
  _In_ LPBYTE    lpProtocol,
  _In_ DWORD     MacType,
  _In_ DWORD     BytesLeft,
  _In_ HPROTOCOL hPreviousProtocol,
  _In_ DWORD     nPreviousProtocolOffset,
  _In_ DWORD     lpInstData
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*hFrame* \[ En\]
</dt> <dd>

Identificador del marco que se está analizando.

</dd> <dt>

*lpFrame* \[ En\]
</dt> <dd>

Puntero al primer byte de un marco.

</dd> <dt>

*lpProtocol* \[ En\]
</dt> <dd>

Puntero al inicio de los datos reconocidos.

</dd> <dt>

*MacType* \[ En\]
</dt> <dd>

Valor MAC del primer protocolo en un marco. *MacType* puede ser uno de los siguientes:



| Value                                                                                                                                                                         | Significado                 |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------|
| <span id="MAC_TYPE_ETHERNET"></span><span id="mac_type_ethernet"></span><dl> <dt>**ETHERNET \_ DE TIPO \_ MAC**</dt> </dl>    | 802.3 <br/>       |
| <span id="MAC_TYPE_TOKENRING"></span><span id="mac_type_tokenring"></span><dl> <dt>**TOKENRING \_ DE \_ TIPO MAC**</dt> </dl> | 802.5 <br/>       |
| <span id="MAC_TYPE_FDDI"></span><span id="mac_type_fddi"></span><dl> <dt>**FDDI \_ DE TIPO \_ MAC**</dt> </dl>                | ANSI X3T9.5 <br/> |



 

</dd> <dt>

*BytesLeft* \[ En\]
</dt> <dd>

Número restante de bytes de un marco que comienza al principio de los datos reconocidos.

</dd> <dt>

*hPreviousProtocol* \[ En\]
</dt> <dd>

Identificador del protocolo anterior.

</dd> <dt>

*nPreviousProtocolOffset* \[ En\]
</dt> <dd>

Desplazamiento del protocolo anterior a partir del principio del marco.

</dd> <dt>

*lpInstData* \[ En\]
</dt> <dd>

Puntero a los datos de instancia que proporciona el protocolo anterior. Los datos de instancia no pueden tener una longitud superior a \_ DWORD PTR.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si la función es correcta, el valor devuelto es un puntero al primer byte después de los datos reconocidos en un marco o **NULL** si los datos reconocidos son el último fragmento de datos de un marco.

Si la función no se realiza correctamente, el valor devuelto es un puntero a los datos reconocidos. El *parámetro lpProtocol* pasa el puntero al archivo DLL del analizador.

## <a name="remarks"></a>Comentarios

Monitor de red llama a **la función AttachProperties** para cada analizador que reconoce un fragmento de datos en un fotograma. Tenga en cuenta que el analizador determina qué propiedades existen en los datos reconocidos y dónde se encuentra cada propiedad.

Durante la implementación de **AttachProperties,** llame [a AttachPropertyInstance](attachpropertyinstance.md) para usar los datos tal como existen en la captura. También puede llamar a la [función AttachPropertyInstanceEx](attachpropertyinstanceex.md) para modificar los datos de propiedad. Sin embargo, se recomienda usar los datos tal como existen en la captura.

Solo se llama a las funciones **AttachPropertyInstanceEx** **y AttachPropertyInstance** para las propiedades que existen en los datos reconocidos. Tenga en Monitor de red una [*base*](p.md) de datos de propiedades para el analizador que contiene una descripción de todas las propiedades que admite el analizador.

**Datos de instancia**

Los datos de instancia son información que se pasa de un analizador a otro. Los datos de instancia pueden ser datos menores o iguales que un PTR DWORD de longitud, o un puntero a datos, como datos de fotogramas sin procesar, que el analizador no necesita asignar o \_ liberar. En el *parámetro lpInstData* de las funciones **AttachProperties** y [RecognizeFrame,](recognizeframe.md) Monitor de red proporciona un puntero a los datos de instancia del protocolo anterior. Puede establecer los datos de instancia del analizador durante la implementación de **RecognizeFrame.**



| Para obtener información acerca de                                          | Vea                                                                |
|-------------------------------------------------------------|--------------------------------------------------------------------|
| Qué son los analizadores y cómo funcionan con Monitor de red.   | [Analizadores](parsers.md)                                             |
| Qué puntos de entrada se incluyen en el archivo DLL del analizador.           | [Arquitectura dll del analizador](parser-dll-architecture.md)             |
| Reconocimiento de datos.                                      | [Implementación de RecognizeFrame](implementing-recognizeframe.md)     |
| Cómo crear una base de datos de propiedades.                          | [Implementar el registro](implementing-register.md)                 |
| La implementación de **AttachProperties**  incluye un ejemplo. | [Implementación de AttachProperties](implementing-attachproperties.md) |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                          |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Netmon.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[AttachPropertyInstance](attachpropertyinstance.md)
</dt> <dt>

[AttachPropertyInstanceEx](attachpropertyinstanceex.md)
</dt> <dt>

[RecognizeFrame](recognizeframe.md)
</dt> </dl>

 

 




