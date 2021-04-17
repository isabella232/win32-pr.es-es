---
description: Representa el Módulo de plataforma segura (TPM), un chip de seguridad de hardware que proporciona una raíz de confianza para un sistema informático.
ms.assetid: da4ba366-49af-420e-a2ad-80bba34b3b00
title: Win32_Tpm (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm
- Win32_Tpm.IsActivated_InitialValue
- Win32_Tpm.IsEnabled_InitialValue
- Win32_Tpm.IsOwned_InitialValue
- Win32_Tpm.SpecVersion
- Win32_Tpm.ManufacturerVersion
- Win32_Tpm.ManufacturerVersionInfo
- Win32_Tpm.ManufacturerId
- Win32_Tpm.PhysicalPresenceVersionInfo
api_type:
- DllExport
api_location:
- Win32_tpm.dll
ms.openlocfilehash: d8d6eac9fba875484ba2f08e149608c9994a1087
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668309"
---
# <a name="win32_tpm-class"></a>\_Clase Win32 TPM

La **clase \_ TPM de Win32** representa el módulo de plataforma segura (TPM), un chip de seguridad de hardware que proporciona una raíz de confianza para un sistema informático.

## <a name="syntax"></a>Sintaxis

``` syntax
class Win32_Tpm
{
  boolean IsActivated_InitialValue;
  boolean IsEnabled_InitialValue;
  boolean IsOwned_InitialValue;
  string  SpecVersion;
  string  ManufacturerVersion;
  string  ManufacturerVersionInfo;
  uint32  ManufacturerId;
  string  PhysicalPresenceVersionInfo;
};
```

## <a name="members"></a>Miembros

La clase **Win32 \_ TPM** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

La clase **Win32 \_ TPM** tiene estos métodos.



| Método                                                                                   | Descripción                                                                                                                                                                                 |
|:-----------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddBlockedCommand**](addblockedcommand-win32-tpm.md)                                 | Agrega un comando de TPM a la lista local de comandos bloqueados en Windows.<br/>                                                                                                             |
| [**ChangeOwnerAuth**](changeownerauth-win32-tpm.md)                                     | Cambia el valor de autorización de propietario de TPM.<br/>                                                                                                                                       |
| [**Claridad**](clear-win32-tpm.md)                                                         | Restablece el TPM a su estado predeterminado de fábrica.<br/>                                                                                                                                     |
| [**ConvertToOwnerAuth**](converttoownerauth-win32-tpm.md)                               | Convierte una frase de contraseña proporcionada por el usuario en un valor de autorización de propietario de 20 bytes que se puede usar para interactuar con el TPM.<br/>                                                            |
| [**CreateEndorsementKeyPair**](createendorsementkeypair-win32-tpm.md)                   | Crea un par de claves de aprobación de 2048 bits en el TPM.<br/>                                                                                                                              |
| [**Disable**](disable-win32-tpm.md)                                                     | Permite al propietario del TPM deshabilitar TPM.<br/>                                                                                                                                         |
| [**Habilitar**](enable-win32-tpm.md)                                                       | Permite al propietario del TPM habilitar TPM.<br/>                                                                                                                                          |
| [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md)               | Obtiene y devuelve la operación de presencia física de TPM pendiente. Use el método [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) para solicitar una operación.<br/> |
| [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md)             | Obtiene y devuelve los resultados de una operación de presencia física de TPM realizada.<br/>                                                                                          |
| [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md)         | Indica la acción del usuario que se necesita para realizar una operación de presencia física de TPM.<br/>                                                                                           |
| [**IsActivated**](isactivated-win32-tpm.md)                                             | Indica si el TPM está activado.<br/>                                                                                                                                          |
| [**IsCommandBlocked**](iscommandblocked-win32-tpm.md)                                   | Indica si el comando TPM puede ejecutarse en este sistema operativo.<br/>                                                                                                              |
| [**IsCommandPresent**](iscommandpresent-win32-tpm.md)                                   | Indica si este equipo admite un comando de TPM.<br/>                                                                                                                   |
| [**IsEnabled**](isenabled-win32-tpm.md)                                                 | Indica si el TPM está habilitado.<br/>                                                                                                                                            |
| [**IsEndorsementKeyPairPresent**](isendorsementkeypairpresent-win32-tpm.md)             | Indica si el TPM tiene un par de claves de aprobación.<br/>                                                                                                                           |
| [**IsOwned**](isowned-win32-tpm.md)                                                     | Indica si el TPM tiene un propietario.<br/>                                                                                                                                          |
| [**IsOwnerClearDisabled**](isownercleardisabled-win32-tpm.md)                           | Indica si el propietario de TPM puede borrar el TPM.<br/>                                                                                                                               |
| [**IsOwnershipAllowed**](isownershipallowed-win32-tpm.md)                               | Indica si se puede instalar un propietario de TPM.<br/>                                                                                                                                  |
| [**IsPhysicalClearDisabled**](isphysicalcleardisabled-win32-tpm.md)                     | Indica si una operación de presencia física de TPM puede borrar el TPM.<br/>                                                                                                           |
| [**IsPhysicalPresenceHardwareEnabled**](isphysicalpresencehardwareenabled-win32-tpm.md) | Indica si este equipo admite una ruta de hardware dedicada para indicar la presencia física.<br/>                                                                                  |
| [**IsSrkAuthCompatible**](issrkauthcompatible-win32-tpm.md)                             | Indica si la autorización de la clave raíz de almacenamiento (SRK) es compatible con Windows.<br/>                                                                                           |
| [**RemoveBlockedCommand**](removeblockedcommand-win32-tpm.md)                           | Quita un comando de TPM de la lista local de comandos bloqueados por Windows.<br/>                                                                                                        |
| [**ResetAuthLockOut**](resetauthlockout-win32-tpm.md)                                   | Restablece el período de tiempo de espera u otro mecanismo que los fabricantes de TPM implementan para protegerse de los ataques de diccionario en el TPM.<br/>                                                 |
| [**ResetSrkAuth**](resetsrkauth-win32-tpm.md)                                           | Restablece el valor de autorización de la clave raíz de almacenamiento (SRK) para que sea compatible con Windows.<br/>                                                                                             |
| [**SelfTest**](selftest-win32-tpm.md)                                                   | Realiza una prueba automática del TPM y devuelve el resultado.<br/>                                                                                                                          |
| [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md)               | Solicita que se ejecute una operación de presencia física de TPM.<br/>                                                                                                                               |
| [**TakeOwnership**](takeownership-win32-tpm.md)                                         | Instala un propietario para el TPM.<br/>                                                                                                                                                   |



 

### <a name="properties"></a>Propiedades

La **clase \_ TPM de Win32** tiene estas propiedades.

<dl> <dt>

**IsActivated \_ InitialValue**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el TPM está activado.

**true** si el dispositivo está activado (es decir, si **IsActivated \_ InitialValue** es true); en caso contrario, **false**.

Este valor se almacena cuando se crea una instancia de la clase. Es posible que el TPM cambie el estado entre la creación de instancias y al comprobar este valor. Para comprobar si el TPM está activado en tiempo real, use el método [**IsActivated**](isactivated-win32-tpm.md) .

**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible.

</dd> <dt>

**IsEnabled \_ InitialValue**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el TPM está habilitado.

**true** si el dispositivo está habilitado (es decir, si **IsEnabled \_ InitialValue** es true); en caso contrario, **false**.

Este valor se almacena cuando se crea una instancia de la clase. Es posible que el TPM cambie el estado entre la creación de instancias y al comprobar este valor. Para comprobar si el TPM está habilitado en tiempo real, use el método [**IsEnabled**](isenabled-win32-tpm.md) .

**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible.

</dd> <dt>

**IsOwned \_ InitialValue**
</dt> <dd> <dl> <dt>

Tipo de datos: **booleano**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Indica si el TPM tiene un propietario.

**true** si el dispositivo tiene un propietario (es decir, si **IsOwned \_ InitialValue** es true); en caso contrario, **false**.

Este valor se almacena cuando se crea una instancia de la clase. Es posible que el TPM cambie el estado entre la creación de instancias y al comprobar este valor. Para comprobar si el TPM es propiedad de tiempo real, use el método [**IsOwned**](isowned-win32-tpm.md) .

**Windows Server 2008 y Windows Vista:** Esta propiedad no está disponible.

</dd> <dt>

**ManufacturerId**
</dt> <dd> <dl> <dt>

Tipo de datos: **UInt32**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La información de identificación que nombra de forma única al fabricante de TPM.

Cuando los datos no están disponibles, se devuelve cero.

Este valor entero se puede traducir en un valor de cadena interpretando cada byte como un carácter ASCII. Por ejemplo, un valor entero de 1414548736 se puede dividir en estos 4 bytes: 0x54, 0x50, 0x4D y 0x00. Suponiendo que la cadena se interpreta de izquierda a derecha, este valor entero se traduce en un valor de cadena de "TPM".

</dd> <dt>

**ManufacturerVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La versión de TPM, tal como la especifica el fabricante.

Cuando los datos no están disponibles, se devuelve "no compatible".

</dd> <dt>

**ManufacturerVersionInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

Otra información de versión específica del fabricante para el TPM.

Cuando los datos no están disponibles, se devuelve "no compatible".

</dd> <dt>

**PhysicalPresenceVersionInfo**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La versión de la interfaz de presencia física, un mecanismo de comunicación que se usa para ejecutar operaciones de dispositivo que requieren presencia física, que el equipo admite.

Esta interfaz debe estar disponible para ejecutar operaciones de presencia física de TPM. Los métodos de **\_ TPM de Win32** [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceRequest**](getphysicalpresencerequest-win32-tpm.md), [**GetPhysicalPresenceTransition**](getphysicalpresencetransition-win32-tpm.md)y [**GetPhysicalPresenceResponse**](getphysicalpresenceresponse-win32-tpm.md) exponen las capacidades de la interfaz de presencia física.

Cuando los datos no están disponibles, se devuelve "no compatible".

</dd> <dt>

**SpecVersion**
</dt> <dd> <dl> <dt>

Tipo de datos: **cadena**
</dt> <dt>

Tipo de acceso: solo lectura
</dt> </dl>

La versión de la especificación Trusted Computing Group (TCG) que admite el TPM. Este valor incluye la versión principal y secundaria de la especificación de TCG, el nivel de revisión de especificación y el nivel de revisión de erratas. Todos los valores están en hexadecimal. Por ejemplo, una información de versión de "1,2, 2, 0" indica que el dispositivo se ha implementado para la especificación de TCG versión 1,2, revisión de nivel 2 y sin erratas.

Cuando los datos no están disponibles, se devuelve "no compatible".

</dd> </dl>

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                      |
| Espacio de nombres<br/>                | \\MicrosoftTpm de \\ seguridad de cimv2 raíz \\<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ TPM. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



 

 
