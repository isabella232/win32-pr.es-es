---
description: La clase WMI SerialPortConfiguration de Win32 representa la configuración de la transmisión de datos en \_ un Windows serie basado en datos. Esto incluye configuraciones para establecer una conexión y una comprobación de errores.
ms.assetid: 688cdcce-8325-4b4d-93ab-5a602e9e3f8e
ms.tgt_platform: multiple
title: Win32_SerialPortConfiguration clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_SerialPortConfiguration
- Win32_SerialPortConfiguration.Caption
- Win32_SerialPortConfiguration.Description
- Win32_SerialPortConfiguration.SettingID
- Win32_SerialPortConfiguration.AbortReadWriteOnError
- Win32_SerialPortConfiguration.BaudRate
- Win32_SerialPortConfiguration.BinaryModeEnabled
- Win32_SerialPortConfiguration.BitsPerByte
- Win32_SerialPortConfiguration.ContinueXMitOnXOff
- Win32_SerialPortConfiguration.CTSOutflowControl
- Win32_SerialPortConfiguration.DiscardNULLBytes
- Win32_SerialPortConfiguration.DSROutflowControl
- Win32_SerialPortConfiguration.DSRSensitivity
- Win32_SerialPortConfiguration.DTRFlowControlType
- Win32_SerialPortConfiguration.EOFCharacter
- Win32_SerialPortConfiguration.ErrorReplaceCharacter
- Win32_SerialPortConfiguration.ErrorReplacementEnabled
- Win32_SerialPortConfiguration.EventCharacter
- Win32_SerialPortConfiguration.IsBusy
- Win32_SerialPortConfiguration.Name
- Win32_SerialPortConfiguration.Parity
- Win32_SerialPortConfiguration.ParityCheckEnabled
- Win32_SerialPortConfiguration.RTSFlowControlType
- Win32_SerialPortConfiguration.StopBits
- Win32_SerialPortConfiguration.XOffCharacter
- Win32_SerialPortConfiguration.XOffXMitThreshold
- Win32_SerialPortConfiguration.XOnCharacter
- Win32_SerialPortConfiguration.XOnXMitThreshold
- Win32_SerialPortConfiguration.XOnXOffInFlowControl
- Win32_SerialPortConfiguration.XOnXOffOutFlowControl
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 065d069b261472e3347a115cfbbff652812b6622
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127174322"
---
# <a name="win32_serialportconfiguration-class"></a>Clase SerialPortConfiguration de Win32 \_

La clase [WMI](../wmisdk/retrieving-a-class.md) **\_ SerialPortConfiguration de Win32** representa la configuración de la transmisión de datos en un Windows serie basado en datos. Esto incluye configuraciones para establecer una conexión y una comprobación de errores.

La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas. Las propiedades se enumeran en orden alfabético, no en orden MOF.

## <a name="syntax"></a>Sintaxis

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4EB-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_SerialPortConfiguration : CIM_Setting
{
  string  Caption;
  string  Description;
  string  SettingID;
  boolean AbortReadWriteOnError;
  uint32  BaudRate;
  boolean BinaryModeEnabled;
  uint32  BitsPerByte;
  boolean ContinueXMitOnXOff;
  boolean CTSOutflowControl;
  boolean DiscardNULLBytes;
  boolean DSROutflowControl;
  boolean DSRSensitivity;
  string  DTRFlowControlType;
  uint32  EOFCharacter;
  uint32  ErrorReplaceCharacter;
  boolean ErrorReplacementEnabled;
  uint32  EventCharacter;
  boolean IsBusy;
  string  Name;
  string  Parity;
  boolean ParityCheckEnabled;
  string  RTSFlowControlType;
  string  StopBits;
  uint32  XOffCharacter;
  uint32  XOffXMitThreshold;
  uint32  XOnCharacter;
  uint32  XOnXMitThreshold;
  uint32  XOnXOffInFlowControl;
  uint32  XOnXOffOutFlowControl;
};
```

## <a name="members"></a>Members

La **clase \_ SerialPortConfiguration de Win32** tiene estos tipos de miembros:

-   [Propiedades](#properties)

### <a name="properties"></a>Propiedades

La **clase \_ SerialPortConfiguration de Win32** tiene estas propiedades.

<dl> <dt>

**AbortReadWriteOnError**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fAbortOnError")
</dt> </dl>

Si **es TRUE,** las operaciones de lectura y escritura finalizan si se produce un error. Si **es TRUE,** el controlador finaliza todas las operaciones de lectura y escritura con un estado de error si se produce un error. El controlador no aceptará ninguna otra operación de comunicación hasta que la aplicación confirme el error.

</dd> <dt>

**Baudrate**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| BaudRate")
</dt> </dl>

Velocidad en baudios (bits por segundo) a la que funciona el dispositivo de comunicaciones.

Ejemplo: 9600

</dd> <dt>

**BinaryModeEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fBinary")
</dt> </dl>

Si **es TRUE,** las transferencias de datos en modo binario están habilitadas para el puerto serie. Los sistemas informáticos que Windows solo permiten transferencias binarias a través de puertos serie, por lo que este valor siempre es **TRUE.**

</dd> <dt>

**BitsPerByte**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ByteSize")
</dt> </dl>

Número de bits transmitidos y recibidos para cada byte de datos para el Windows serie. El número puede variar con los bits de corrección de errores y de control, como los bits de paridad.

Ejemplo: 8

</dd> <dt>

**Caption**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64)
</dt> </dl>

Breve descripción textual del objeto actual.

Esta propiedad se hereda de la [**configuración de CIM \_**](cim-setting.md).

</dd> <dt>

**ContinueXMitOnXOff**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de comunicación de Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fTXContinueOnXoff")
</dt> </dl>

Si **es TRUE,** las transmisiones de datos continúan cuando el búfer de entrada se encuentra dentro de los bytes **XOffXMitThreshold** de estar lleno y el controlador ha transmitido el valor **XOffCharmitter** para dejar de recibir bytes. Si **es FALSE,** la transmisión no continúa hasta que el búfer de entrada está dentro de los bytes **XOnXMitThreshold** de estar vacío y el controlador ha transmitido el valor **XOnCharacter** para reanudar la recepción.

</dd> <dt>

**CTSOutflowControl**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxCtsFlow")
</dt> </dl>

Si **es TRUE,** se comprueba la señal clear to send (CTS) antes de transmitir los datos. CTS indica que ambos dispositivos de la conexión serie están listos para transferir datos. La transmisión de datos se suspende hasta que se da la señal CTS.

</dd> <dt>

**Descripción**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Descripción textual del objeto actual.

Esta propiedad se hereda de la [**configuración de CIM \_**](cim-setting.md).

</dd> <dt>

**DiscardNULLBytes**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fNull")
</dt> </dl>

Si **es TRUE,** los bytes **NULL** (caracteres) se descartan cuando se reciben.

</dd> <dt>

**DSROutflowControl**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de comunicación de Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutxDsrFlow")
</dt> </dl>

Si **es TRUE,** el control de flujo de salida de datos se habilita cuando hay una condición lista para el conjunto de datos (DSR). DSR indica que los dispositivos han establecido la conexión en la conexión serie. La transmisión de datos DSR se suspende hasta que se da la señal DSR.

</dd> <dt>

**DSRSensitivity**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de comunicación de Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDsrSensitivity")
</dt> </dl>

Si **es TRUE,** el controlador de comunicaciones es sensible al estado de la señal DSR. El controlador omite los bytes recibidos, a menos que la línea de entrada del módem DSR sea alta.

</dd> <dt>

**DTRFlowControlType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fDtrControl")
</dt> </dl>

Uso del control de flujo listo para terminal de datos (DTR) una vez establecida una conexión.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

**Habilitar** ("Habilitar")


</dt> <dd></dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

**Disable** ("Disable")


</dt> <dd></dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

**Protocolo de enlace** ("protocolo de enlace")


</dt> <dd></dd> </dl>

</dd> <dt>

**EOFCharacter**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EofChar")
</dt> </dl>

Valor del carácter utilizado para indicar el final de los datos.

Ejemplo: ^Z

</dd> <dt>

**ErrorReplaceCharacter**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| ErrorChar")
</dt> </dl>

Valor del carácter utilizado para reemplazar los bytes recibidos por un error de paridad.

Ejemplo: ^C

</dd> <dt>

**ErrorReplacementEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de comunicación de Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fErrorChar")
</dt> </dl>

Si **es TRUE,** los bytes recibidos con errores de paridad se reemplazan por el **valor ErrorReplaceCharacter.** Los caracteres con errores de paridad solo se reemplazan si esta propiedad es **TRUE** y la paridad está habilitada.

</dd> <dt>

**EventCharacter**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de comunicación de Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| EvtChar")
</dt> </dl>

Valor del carácter de control que se usa para señalar un evento, como el final del archivo.

Ejemplo: ^e

</dd> <dt>

**IsBusy**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("CreateFile de funciones de archivo \| \| Win32API")
</dt> </dl>

Si **es TRUE,** el puerto serie está ocupado.

</dd> <dt>

**Nombre**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**key**](../wmisdk/key-qualifier.md), [**MaxLen**](../wmisdk/standard-qualifiers.md) (256), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| Hardware \\ \\ DeviceMap \\ \\ SerialComm")
</dt> </dl>

Nombre del puerto Windows serie.

Ejemplo: "COM1"

</dd> <dt>

**Parity**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Paridad dcB de estructuras de comunicación de Win32API") \| \| [](/windows/win32/api/winbase/ns-winbase-dcb) \|
</dt> </dl>

Método de comprobación de paridad que se va a usar. La paridad se usa como una técnica de comprobación de errores en la que se incluye un bit de paridad adicional con cada unidad de datos. A continuación, el receptor puede comprobar la validez de los datos contando los bits que se establecen.

<dt>

<span id="None"></span><span id="none"></span><span id="NONE"></span>

<span id="None"></span><span id="none"></span><span id="NONE"></span>**None** ("None")


</dt> <dd>

No se usa la comprobación de paridad.

</dd> <dt>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>

<span id="Odd"></span><span id="odd"></span><span id="ODD"></span>**Impar** ("Impar")


</dt> <dd>

Establece el bit de paridad de forma que el recuento de bits establecidos sea un número impar.

</dd> <dt>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>

<span id="Even"></span><span id="even"></span><span id="EVEN"></span>**Incluso** ("Even")


</dt> <dd>

Establece el bit de paridad de forma que el recuento de bits establecidos sea un número par.

</dd> <dt>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>

<span id="Mark"></span><span id="mark"></span><span id="MARK"></span>**Mark** ("Mark")


</dt> <dd>

Establece el conjunto de bits de paridad en 1.

</dd> <dt>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>

<span id="Space"></span><span id="space"></span><span id="SPACE"></span>**Espacio** ("Espacio")


</dt> <dd>

Deja el bit de paridad establecido en 0 (cero).

</dd> </dl>

</dd> <dt>

**ParityCheckEnabled**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de comunicación de Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fParity")
</dt> </dl>

Si **es TRUE,** la comprobación de paridad está habilitada.

</dd> <dt>

**RTSFlowControlType**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Solicitud para enviar el control de flujo (RTS). RTS se usa para indicar que los datos están disponibles para la transmisión.

<dt>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>

<span id="Enable"></span><span id="enable"></span><span id="ENABLE"></span>**Habilitar** ("Habilitar")


</dt> <dd>

RTS se deja en para la sesión de transferencia de datos.

</dd> <dt>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>

<span id="Disable"></span><span id="disable"></span><span id="DISABLE"></span>**Deshabilitar** ("Deshabilitar")


</dt> <dd>

RtS se omite después de recibir la primera señal RTS.

</dd> <dt>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>

<span id="Handshake"></span><span id="handshake"></span><span id="HANDSHAKE"></span>**Protocolo de enlace** ("protocolo de enlace")


</dt> <dd>

RTS se apaga si el búfer de transmisión está lleno más de tres cuartos y RTS está activado cuando el búfer está menos de la mitad lleno.

</dd> <dt>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>

<span id="Toggle"></span><span id="toggle"></span><span id="TOGGLE"></span>**Alternar** ("Alternar")


</dt> <dd>

RTS está activado si hay datos almacenados en búfer para la transmisión.

</dd> </dl>

</dd> <dt>

**SettingID**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MaxLen**](../wmisdk/standard-qualifiers.md) (256)
</dt> </dl>

Identificador por el que se conoce el objeto actual.

Esta propiedad se hereda de cim [**\_ setting**](cim-setting.md).

</dd> <dt>

**StopBits**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de comunicación de Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| StopBits")
</dt> </dl>

Número de bits de detención que se usarán. Los bits de detenerse separan cada unidad de datos en una conexión serie asincrónica. También se envían continuamente cuando no hay datos disponibles para la transmisión.

<dt>

<span id="1"></span>

**1** ("1")


</dt> <dd></dd> <dt>

<span id="1.5"></span>

**1.5** ("1.5")


</dt> <dd></dd> <dt>

<span id="2"></span>

**2** ("2")


</dt> <dd></dd> </dl>

</dd> <dt>

**XOffCharacter**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de comunicación de Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffChar")
</dt> </dl>

Valor del carácter XOFF para la transmisión y la recepción. XOFF es un control de software para detener la transmisión de datos (mientras que RTS y CTS son controles de hardware). XON reanuda la transmisión.

</dd> <dt>

**XOffXMitThreshold**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XoffLim")
</dt> </dl>

Número máximo de bytes permitidos en el búfer de entrada antes de que se envíe el carácter XOFF.

</dd> <dt>

**XOnCharacter**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Estructuras de comunicación de Win32API \| \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonChar")
</dt> </dl>

Valor del carácter XON para la transmisión y la recepción. XON es un control de software para reanudar la transmisión de datos (mientras que RTS y CTS son controles de hardware). XOFF detiene la transmisión.

</dd> <dt>

**XOnXMitThreshold**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| XonLim")
</dt> </dl>

Número mínimo de bytes permitidos en el búfer de entrada antes de que se envíe el carácter XON. Esta propiedad funciona junto con **XOffXMitThreshold para** regular la velocidad a la que se transfieren los datos.

</dd> <dt>

**XOnXOffInFlowControl**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fInX")
</dt> </dl>

Si **es TRUE,** se usa el control de flujo XON/XOFF durante la recepción. Si **es TRUE,** el valor **XOffCharacter** se envía cuando el búfer de entrada entra dentro de los bytes **XOffXMitThreshold** de estar lleno y el valor **de XOnCharacter** se envía cuando el búfer de entrada entra dentro de los bytes **XOnXMitThreshold** de estar vacío.

<dt>

<span id="0"></span>

<span id="0"></span>**0**


</dt> <dd>

false

</dd> <dt>

<span id="1"></span>

<span id="1"></span>**1**


</dt> <dd>

true

</dd> </dl>

</dd> <dt>

**XOnXOffOutFlowControl**
</dt> <dd> <dl> <dt>

Tipo de datos: **uint32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> <dt>

Calificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API \| Communication Structures \| [**DCB**](/windows/win32/api/winbase/ns-winbase-dcb) \| fOutX")
</dt> </dl>

**XOnXOffOutFlowControl** especifica si se usa el control de flujo XON o XOFF durante la transmisión. Si **es TRUE,** la transmisión se detiene cuando se recibe el valor **XOffCharacter** y se inicia de nuevo cuando se recibe el valor **XOnCharacter.**

</dd> </dl>

## <a name="remarks"></a>Observaciones

La **clase \_ SerialPortConfiguration de Win32** se deriva de [**cim \_ setting**](cim-setting.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                          |
| Espacio de nombres<br/>                | \\CIMV2 raíz<br/>                                                                  |
| MOF<br/>                      | <dl> <dt>CIMWin32.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>CIMWin32.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Configuración de CIM \_**](cim-setting.md)
</dt> <dt>

[Clases de hardware del sistema de equipo](computer-system-hardware-classes.md)
</dt> </dl>

 

 
