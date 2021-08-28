---
description: Aprenda a trabajar con dispositivos NVMe de alta velocidad desde Windows aplicación.
ms.assetid: 037AF841-C2C9-4551-9CCB-F2A2F199083A
title: Trabajar con unidades NVMe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22a749764aa0874aef618558199ca418582d0d36
ms.sourcegitcommit: 0dec0044816af3f2b2e6403659e1cf11138c90cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/13/2021
ms.locfileid: "121812863"
---
# <a name="working-with-nvme-drives"></a>Trabajar con unidades NVMe

**Se aplica a:**

-   Windows 10
-   Windows Server 2016

Aprenda a trabajar con dispositivos NVMe de alta velocidad desde Windows aplicación. El acceso al dispositivo se **habilita a** travésStorNVMe.sys, el controlador que se introdujo por primera vez en Windows Server 2012 R2 y Windows 8.1. También está disponible para 7 dispositivos Windows a través de una corrección de kb. En Windows 10, se presentaron varias características nuevas, incluido un mecanismo de paso a través para comandos NVMe específicos del proveedor y actualizaciones de las ICTL existentes.

En este tema se proporciona información general sobre las API de uso general que puede usar para acceder a las unidades NVMe Windows 10. También se describe lo siguiente:

-   Envío de un comando NVMe específico del proveedor con [paso a través](#pass-through-mechanism)
-   Cómo enviar [un comando Identificar, Obtener características u Obtener páginas](#protocol-specific-queries) de registro a la unidad NVMe
-   Cómo obtener [información de temperatura de](#temperature-queries) una unidad NVMe
-   Cómo realizar comandos de cambio de comportamiento, como establecer [umbrales de temperatura](#behavior-changing-commands)

## <a name="apis-for-working-with-nvme-drives"></a>API para trabajar con unidades NVMe

Puede usar las siguientes API de uso general para acceder a las unidades NVMe en Windows 10. Estas API se pueden encontrar en **winioctl.h** para aplicaciones en modo de usuario y **ntddstor.h** para controladores de modo kernel. Para obtener más información sobre los archivos de encabezado, vea [Archivos de encabezado](#header-files).

-   [**IOCTL \_ COMANDO \_ DE PROTOCOLO DE \_ ALMACENAMIENTO:**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) use esta IOCTL con la estructura **DE COMANDOS DEL PROTOCOLO \_ \_ DE** ALMACENAMIENTO para emitir comandos NVMe. Esta IOCTL habilita el paso a través de NVMe y admite el registro de efectos de comando en NVMe. Puede usarlo con comandos específicos del proveedor. Para obtener más información, vea [Mecanismo de paso a través](#pass-through-mechanism).

-   [**ALMACENAMIENTO \_ COMANDO \_ PROTOCOL:**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) esta estructura de búfer de entrada incluye un **campo ReturnStatus** que se puede usar para notificar los siguientes valores de estado.
    -   **ESTADO DEL \_ PROTOCOLO \_ DE ALMACENAMIENTO \_ PENDIENTE**
    -   **ESTADO CORRECTO \_ \_ DEL PROTOCOLO DE \_ ALMACENAMIENTO**
    -   **ERROR DE \_ ESTADO DEL PROTOCOLO DE \_ \_ ALMACENAMIENTO**
    -   **SOLICITUD DE \_ ESTADO DE PROTOCOLO DE ALMACENAMIENTO NO \_ \_ \_ VÁLIDA**
    -   **ESTADO \_ DEL PROTOCOLO DE ALMACENAMIENTO SIN \_ \_ \_ DISPOSITIVO**
    -   **ESTADO DEL \_ PROTOCOLO \_ DE ALMACENAMIENTO \_ OCUPADO**
    -   **SATURACIÓN \_ DE DATOS DE ESTADO DEL PROTOCOLO DE \_ \_ \_ ALMACENAMIENTO**
    -   **ESTADO DEL \_ PROTOCOLO \_ DE ALMACENAMIENTO \_ INSUFICIENTE \_**
    -   **ESTADO DEL \_ PROTOCOLO DE ALMACENAMIENTO NO \_ \_ \_ ADMITIDO**
-   [**IOCTL \_ STORAGE \_ QUERY \_ PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) : use esta IOCTL con la estructura STORAGE PROPERTY **\_ \_ QUERY** para recuperar información del dispositivo. Para obtener más información, vea [Consultas específicas del protocolo y](#protocol-specific-queries) Consultas de [temperatura](#temperature-queries).

-   [**ALMACENAMIENTO \_ PROPERTY \_ QUERY:**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) esta estructura incluye los **campos PropertyId** y **AdditionalParameters** para especificar los datos que se deben consultar. En el **propertyId** que se ha archivo, use la **enumeración STORAGE \_ PROPERTY \_ ID** para especificar el tipo de datos. Use el **campo AdditionalParameters** para especificar más detalles, en función del tipo de datos. Para los datos específicos del protocolo, use la estructura **STORAGE \_ PROTOCOL SPECIFIC \_ \_ DATA** en el **campo AdditionalParameters.** Para los datos de temperatura, use la **estructura STORAGE \_ TEMPERATURE \_ INFO** en el **campo AdditionalParameters.**
-   [**ALMACENAMIENTO \_ PROPERTY \_ ID**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) : esta enumeración incluye nuevos valores que permiten a **IOCTL STORAGE QUERY \_ \_ \_ PROPERTY** recuperar información específica del protocolo y la temperatura.

    -   **StorageAdapterProtocolSpecificProperty**: si ProtocolType = ProtocolTypeNvme y DataType = NVMeDataTypeLogPage, los llamadores deben solicitar fragmentos de datos de 512 bytes.
    -   **StorageDeviceProtocolSpecificProperty**

    Use uno de estos identificadores de propiedad específicos del protocolo en combinación con **STORAGE \_ PROTOCOL SPECIFIC \_ \_ DATA** para recuperar datos específicos del protocolo en la estructura DEL DESCRIPTOR DE DATOS [**DEL PROTOCOLO \_ \_ \_ DE**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) ALMACENAMIENTO.

    -   **StorageAdapterTemperatureProperty**
    -   **StorageDeviceTemperatureProperty**

    Use uno de estos identificadores de propiedad de temperatura para recuperar datos de temperatura en la [**estructura DEL DESCRIPTOR DE DATOS DE TEMPERATURA \_ \_ \_ DE**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) ALMACENAMIENTO.

-   [**ALMACENAMIENTO \_ DATOS \_ ESPECÍFICOS \_ DEL**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) PROTOCOLO: recupere datos específicos de NVMe cuando se utilice esta estructura para el campo **AdditionalParameters** de **STORAGE PROPERTY \_ \_ QUERY** y se especifique un valor de enumeración STORAGE [**PROTOCOL \_ \_ NVME DATA \_ \_ TYPE.**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) Use uno de los siguientes valores **de \_ STORAGE PROTOCOL \_ NVME DATA \_ \_ TYPE** en el **campo DataType** de la **estructura STORAGE PROTOCOL SPECIFIC \_ \_ \_ DATA:**

    -   Use **NVMeDataTypeIdentify para obtener** los datos de Identify Controller o Identify Namespace.
    -   Use **NVMeDataTypeLogPage para** obtener páginas de registro (incluidos los datos smart/health).
    -   Use **NVMeDataTypeFeature para** obtener características de la unidad NVMe.

-   [**ALMACENAMIENTO \_ INFORMACIÓN \_ DE TEMPERATURA:**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) esta estructura se usa para contener datos de temperatura específicos. Se usa en el DESCRIPTOR DE DATOS **STORAGE \_ \_ \_ LAATURE** para devolver los resultados de una consulta de temperatura.

-   [**IOCTL \_ UMBRAL \_ DE TEMPERATURA DEL CONJUNTO \_ \_ DE**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) ALMACENAMIENTO: use esta IOCTL con la estructura **UMBRAL DE TEMPERATURA \_ \_ DE** ALMACENAMIENTO para establecer umbrales de temperatura. Para obtener más información, vea [Behavior changing commands (Cambio de comportamiento de comandos).](#behavior-changing-commands)

-   [**ALMACENAMIENTO \_ UMBRAL \_ DE TEMPERATURA:**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) esta estructura se usa como búfer de entrada para especificar el umbral de temperatura. El **campo OverThreshold** (booleano) especifica si el campo **Umbral** es el valor de umbral por encima del umbral o no (de lo contrario, es el valor inferior al umbral).

## <a name="pass-through-mechanism"></a>Mecanismo de paso a través

Los comandos que no se definen en la especificación NVMe son los más difíciles de controlar para el sistema operativo host: el host no tiene información sobre los efectos que pueden tener los comandos en el dispositivo de destino, la infraestructura expuesta (espacios de nombres o tamaños de bloque) y su comportamiento.

Para llevar mejor estos comandos específicos del dispositivo a través de la pila de almacenamiento Windows, un nuevo mecanismo de paso a través permite canalizar comandos específicos del proveedor. Esta canalización de paso a través también ayudará al desarrollo de herramientas de administración y pruebas. Sin embargo, este mecanismo de paso a través requiere el uso del registro de efectos de comando. Además, StoreNVMe.sys requiere que todos los comandos, no solo los comandos de paso a través, se describa en el registro de efectos de comando.

> [!IMPORTANT]
> StorNVMe.sys y Storport.sys bloquearán cualquier comando en un dispositivo si no se describe en el registro de efectos de comando.

 

### <a name="supporting-the-command-effects-log"></a>Compatibilidad con el registro de efectos de comando

El registro de efectos de comando (como se describe en Comandos admitidos y efectos, sección 5.10.1.5 de la especificación [NVMe 1.2)](https://nvmexpress.org/specifications)permite la descripción de los efectos de los comandos específicos del proveedor junto con los comandos definidos por la especificación. Esto facilita tanto la validación de compatibilidad de comandos como la optimización del comportamiento de los comandos y, por tanto, se debe implementar para todo el conjunto de comandos que admite el dispositivo. Las condiciones siguientes describen el resultado sobre cómo se envía el comando en función de su entrada de registro de efectos de comando.

Para cualquier comando específico descrito en el registro de efectos de comando...

**While**:

-   El comando Compatible (CSUPP) se establece en "1", lo que significa que el controlador admite el comando (bit 01)

    > [!Note]  
    > Cuando CSUPP se establece en "0" (lo que significa que no se admite el comando), el comando se bloqueará.

     

**Y si** se establece alguna de las siguientes opciones:

-   El cambio de funcionalidad del controlador (CCI) se establece en "1", lo que significa que el comando puede cambiar las funcionalidades del controlador (bit 04)

-   El cambio de inventario de espacios de nombres (NIC) se establece en "1", lo que significa que el comando puede cambiar el número o las funcionalidades de varios espacios de nombres (bit 03)

-   El cambio de funcionalidad del espacio de nombres (NCC) se establece en "1", lo que significa que el comando puede cambiar las funcionalidades de un único espacio de nombres (bit 02)

-   Envío y ejecución de comandos (CSE) se establece en 001b o 010b, lo que significa que el comando se puede enviar cuando no hay ningún otro comando pendiente en el mismo espacio de nombres o en cualquier otro, y que no se debe enviar otro comando al mismo espacio de nombres o a ningún espacio de nombres hasta que se complete este comando (Bits 18:16)

**A** continuación, el comando se enviará como el único comando pendiente para el adaptador.

**De lo contrario, si**:

-   Envío y ejecución de comandos (CSE) se establece en 001b, lo que significa que el comando se puede enviar cuando no hay ningún otro comando pendiente en el mismo espacio de nombres y que no se debe enviar otro comando al mismo espacio de nombres hasta que se complete este comando (Bits 18:16)

**A** continuación, el comando se enviará como el único comando pendiente al objeto Número de unidad lógica (LUN).

**De** lo contrario, el comando se envía con otros comandos pendientes sin inhibición. Por ejemplo, si se envía un comando específico del proveedor al dispositivo para recuperar información estadística que no está definida por la especificación, no debería haber ningún riesgo para cambiar el comportamiento o la capacidad del dispositivo para ejecutar comandos de E/S. Estas solicitudes se podrían atender en paralelo a la E/S y no sería necesario pausar y reanudar.

### <a name="using-ioctl_storage_protocol_command-to-send-commands"></a>Uso de IOCTL \_ STORAGE PROTOCOL COMMAND para enviar \_ \_ comandos

El paso a través se puede realizar mediante el comando [**IOCTL \_ STORAGE PROTOCOL \_ \_ ,**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command)introducido en Windows 10. Esta IOCTL se diseñó para tener un comportamiento similar al de las ICTL de paso a través de SCSI y ATA existentes, para enviar un comando incrustado al dispositivo de destino. A través de esta IOCTL, el paso a través se puede enviar a un dispositivo de almacenamiento, incluida una unidad NVMe.

Por ejemplo, en NVMe, la IOCTL permitirá el envío de los siguientes códigos de comando.

-   Comandos de administrador específicos del proveedor (C0h – FFh)
-   Comandos NVMe específicos del proveedor (80 h – FFh)

Al igual que con todas las demás IOCTL, use [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) para enviar la IOCTL de paso a través hacia abajo. La IOCTL se rellena mediante la estructura de búfer de entrada COMANDO DE PROTOCOLO DE [**\_ \_ ALMACENAMIENTO**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) que se encuentra en **ntddstor.h**. Rellene el **campo** Comando con el comando específico del proveedor.


```C++
typedef struct _STORAGE_PROTOCOL_COMMAND {

    ULONG   Version;                        // STORAGE_PROTOCOL_STRUCTURE_VERSION
    ULONG   Length;                         // sizeof(STORAGE_PROTOCOL_COMMAND)

    STORAGE_PROTOCOL_TYPE  ProtocolType;
    ULONG   Flags;                          // Flags for the request

    ULONG   ReturnStatus;                   // return value
    ULONG   ErrorCode;                      // return value, optional

    ULONG   CommandLength;                  // non-zero value should be set by caller
    ULONG   ErrorInfoLength;                // optional, can be zero
    ULONG   DataToDeviceTransferLength;     // optional, can be zero. Used by WRITE type of request.
    ULONG   DataFromDeviceTransferLength;   // optional, can be zero. Used by READ type of request.

    ULONG   TimeOutValue;                   // in unit of seconds

    ULONG   ErrorInfoOffset;                // offsets need to be pointer aligned
    ULONG   DataToDeviceBufferOffset;       // offsets need to be pointer aligned
    ULONG   DataFromDeviceBufferOffset;     // offsets need to be pointer aligned

    ULONG   CommandSpecific;                // optional information passed along with Command.
    ULONG   Reserved0;

    ULONG   FixedProtocolReturnData;        // return data, optional. Some protocol, such as NVMe, may return a small amount data (DWORD0 from completion queue entry) without the need of separate device data transfer.
    ULONG   Reserved1[3];

    _Field_size_bytes_full_(CommandLength) UCHAR Command[ANYSIZE_ARRAY];

} STORAGE_PROTOCOL_COMMAND, *PSTORAGE_PROTOCOL_COMMAND;
```



El comando específico del proveedor que se desea enviar debe rellenarse en el campo resaltado anterior. Tenga en cuenta de nuevo que el registro de efectos de comando debe implementarse para los comandos de paso a través. En concreto, estos comandos deben ser notificados como admitidos en el registro de efectos de comando (consulte la sección anterior para obtener más información). Tenga en cuenta también que los campos PRP son específicos del controlador, por lo que las aplicaciones que envían comandos pueden dejarlos como 0.

Por último, esta IOCTL de paso a través está pensada para enviar comandos específicos del proveedor. Para enviar otros comandos NVMe específicos de administrador o que no sean de proveedor, como Identificar, no se debe usar esta IOCTL de paso a través. Por ejemplo, **se debe usar IOCTL STORAGE QUERY \_ \_ \_ PROPERTY** para identificar u obtener páginas de registro. Para obtener más información, vea la sección siguiente, [Consultas específicas del protocolo](/windows).

### <a name="dont-update-firmware-through-the-pass-through-mechanism"></a>No actualizar el firmware a través del mecanismo de paso a través

Los comandos de descarga y activación de firmware no deben enviarse mediante el paso a través. **IOCTL \_ STORAGE \_ PROTOCOL \_ COMMAND solo** debe usarse para comandos específicos del proveedor.

En su lugar, use las siguientes ICTL de almacenamiento general (introducidas en Windows 10) para evitar que las aplicaciones usen directamente la versión de minipuerto SCSI de \_ firmware IOCTL. Storage los controladores traducirán la IOCTL a un comando SCSI o a la versión de minipuerto SCSI de \_ la IOCTL al minipuerto.

Estas IOCTL se recomiendan para desarrollar herramientas de actualización de firmware en Windows 10 y Windows Server 2016:

-   [**IOCTL \_ STORAGE \_ FIRMWARE \_ GET \_ INFO**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
-   [**DESCARGA DE \_ FIRMWARE DE ALMACENAMIENTO \_ DE IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
-   [**ACTIVACIÓN DEL \_ FIRMWARE DE \_ ALMACENAMIENTO DE IOCTL \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)

Para obtener información de almacenamiento y actualizar el firmware, Windows también admite cmdlets de PowerShell para hacerlo rápidamente:

-   `Get-StorageFirmwareInfo`
-   `Update-StorageFirmware `

> [!Note]  
> Para actualizar el firmware en NVMe en Windows 8.1, use EL FIRMWARE DE MINIPORT DE IOCTL \_ \_ \_ SCSI. Esta IOCTL no se ha reportado a Windows 7. Para obtener más información, consulte [Actualización de firmware para un dispositivo NVMe en Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).

 

### <a name="returning-errors-through-the-pass-through-mechanism"></a>Devolver errores a través del mecanismo de paso a través

De forma similar a los IOCTLs de paso a través de SCSI y ATA, cuando se envía un comando o solicitud al minipuerto o dispositivo, la IOCTL devuelve si se ha realizado correctamente o no. En la [**estructura DE COMANDOS DEL PROTOCOLO \_ \_ DE**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) ALMACENAMIENTO, la IOCTL devuelve el estado a través del **campo ReturnStatus.**

### <a name="example-sending-a-vendor-specific-command"></a>Ejemplo: envío de un comando específico del proveedor

En este ejemplo, se envía un comando arbitrario específico del proveedor (0xFF) a través de paso a una unidad NVMe. El código siguiente asigna un búfer, inicializa una consulta y, a continuación, envía el comando al dispositivo a través de DeviceIoControl.


```C++
    ZeroMemory(buffer, bufferLength);  
    protocolCommand = (PSTORAGE_PROTOCOL_COMMAND)buffer;  

    protocolCommand->Version = STORAGE_PROTOCOL_STRUCTURE_VERSION;  
    protocolCommand->Length = sizeof(STORAGE_PROTOCOL_COMMAND);  
    protocolCommand->ProtocolType = ProtocolTypeNvme;  
    protocolCommand->Flags = STORAGE_PROTOCOL_COMMAND_FLAG_ADAPTER_REQUEST;  
    protocolCommand->CommandLength = STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->ErrorInfoLength = sizeof(NVME_ERROR_INFO_LOG);  
    protocolCommand->DataFromDeviceTransferLength = 4096;  
    protocolCommand->TimeOutValue = 10;  
    protocolCommand->ErrorInfoOffset = FIELD_OFFSET(STORAGE_PROTOCOL_COMMAND, Command) + STORAGE_PROTOCOL_COMMAND_LENGTH_NVME;  
    protocolCommand->DataFromDeviceBufferOffset = protocolCommand->ErrorInfoOffset + protocolCommand->ErrorInfoLength;  
    protocolCommand->CommandSpecific = STORAGE_PROTOCOL_SPECIFIC_NVME_ADMIN_COMMAND;  

    command = (PNVME_COMMAND)protocolCommand->Command;  

    command->CDW0.OPC = 0xFF;  
    command->u.GENERAL.CDW10 = 0xto_fill_in;  
    command->u.GENERAL.CDW12 = 0xto_fill_in;  
    command->u.GENERAL.CDW13 = 0xto_fill_in;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_PROTOCOL_COMMAND,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL 
                             );  
```



En este ejemplo, se espera `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` si el comando se ha instalado correctamente en el dispositivo.

## <a name="protocol-specific-queries"></a>Consultas específicas del protocolo

Windows 8.1 introdujo [**LA PROPIEDAD DE CONSULTA DE ALMACENAMIENTO \_ DE IOCTL \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) para la recuperación de datos. En Windows 10, la IOCTL se mejoró para admitir las características NVMe solicitadas habitualmente, como Obtener páginas de **registro,** Obtener características e **Identificar**. Esto permite la recuperación de información específica de NVMe con fines de supervisión e inventario.

El búfer de entrada para la IOCTL, [**STORAGE \_ PROPERTY \_ QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) (desde Windows 10) se muestra aquí.


```C++
typedef struct _STORAGE_PROPERTY_QUERY {
    STORAGE_PROPERTY_ID PropertyId;
    STORAGE_QUERY_TYPE QueryType;
    UCHAR  AdditionalParameters[1];
} STORAGE_PROPERTY_QUERY, *PSTORAGE_PROPERTY_QUERY;
```



Al usar LA PROPIEDAD DE CONSULTA DE ALMACENAMIENTO DE IOCTL para recuperar información específica del protocolo NVMe en el [**\_ \_ \_ DESCRIPTOR**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor)DE DATOS DEL PROTOCOLO DE ALMACENAMIENTO, configure la estructura [**STORAGE PROPERTY \_ \_ QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) como se muestra a continuación: [**\_ \_ \_**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property)

-   Asigne un búfer que pueda tener una estructura [**STORAGE \_ PROPERTY QUERY \_ y**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) [**una estructura STORAGE PROTOCOL SPECIFIC \_ \_ \_ DATA.**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data)

-   Establezca el **campo PropertyID** en **StorageAdapterProtocolSpecificProperty** o **StorageDeviceProtocolSpecificProperty** para una solicitud de controlador o dispositivo o espacio de nombres, respectivamente.

-   Establezca el **campo QueryType** en **PropertyStandardQuery.**

-   Rellene la [**estructura STORAGE PROTOCOL SPECIFIC \_ \_ \_ DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) con los valores deseados. El inicio de STORAGE **\_ PROTOCOL SPECIFIC DATA \_ \_ es** el **campo AdditionalParameters** de [**STORAGE PROPERTY \_ \_ QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).

La [**estructura DE DATOS \_ \_ \_ ESPECÍFICOS DEL**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) PROTOCOLO DE ALMACENAMIENTO (Windows 10) se muestra aquí.


```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                 

    ULONG   ProtocolDataRequestValue;
    ULONG   ProtocolDataRequestSubValue;

    ULONG   ProtocolDataOffset;         
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;   
    ULONG   Reserved[3];

} STORAGE_PROTOCOL_SPECIFIC_DATA, *PSTORAGE_PROTOCOL_SPECIFIC_DATA;
```



Para especificar un tipo de información específica del protocolo NVMe, configure la estructura [**STORAGE \_ PROTOCOL SPECIFIC \_ \_ DATA**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) como se muestra a continuación:

-   Establezca el **campo ProtocolType** en **ProtocolTypeNVMe**.

-   Establezca el **campo DataType** en un valor de enumeración definido por [**STORAGE PROTOCOL \_ \_ NVME DATA \_ \_ TYPE**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type):

    -   Use **NVMeDataTypeIdentify para obtener** los datos de Identify Controller o Identify Namespace.
    -   Use **NVMeDataTypeLogPage para** obtener páginas de registro (incluidos los datos smart/health).
    -   Use **NVMeDataTypeFeature para** obtener características de la unidad NVMe.

Cuando **se usa ProtocolTypeNVMe** como **ProtocolType**, las consultas de información específica del protocolo se pueden recuperar en paralelo con otras E/S en la unidad NVMe.

> [!IMPORTANT]
> Para un [**IOCTL_STORAGE_QUERY_PROPERTY**](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property) que usa un **STORAGE_PROPERTY_ID** de [**StorageAdapterProtocolSpecificProperty**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id)y cuya estructura [**STORAGE_PROTOCOL_SPECIFIC_DATA**](/windows/win32/api/winioctl/ns-winioctl-storage_protocol_specific_data) o [**STORAGE_PROTOCOL_SPECIFIC_DATA_EXT**](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-storage_protocol_specific_data_ext) se establece en y , establezca el miembro ProtocolDataLength de esa misma estructura en un valor mínimo de `ProtocolType=ProtocolTypeNvme` `DataType=NVMeDataTypeLogPage` 512 (bytes).


En los ejemplos siguientes se muestran las consultas específicas del protocolo NVMe.

### <a name="example-nvme-identify-query"></a>Ejemplo: Consulta de identificación de NVMe

En este ejemplo, la **solicitud Identificar** se envía a una unidad NVMe. El código siguiente inicializa la estructura de datos de consulta y, a continuación, envía el comando al dispositivo a través de DeviceIoControl.


```C++
    BOOL    result;
    PVOID   buffer = NULL;
    ULONG   bufferLength = 0;
    ULONG   returnedLength = 0;

    PSTORAGE_PROPERTY_QUERY query = NULL;
    PSTORAGE_PROTOCOL_SPECIFIC_DATA protocolData = NULL;
    PSTORAGE_PROTOCOL_DATA_DESCRIPTOR protocolDataDescr = NULL;

    //
    // Allocate buffer for use.
    //
    bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_QUERY, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA) + NVME_MAX_LOG_SIZE;
    buffer = malloc(bufferLength);

    if (buffer == NULL) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: allocate buffer failed, exit.\n"));
        goto exit;
    }

    //
    // Initialize query data structure to get Identify Controller Data.
    //
    ZeroMemory(buffer, bufferLength);

    query = (PSTORAGE_PROPERTY_QUERY)buffer;
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;

    query->PropertyId = StorageAdapterProtocolSpecificProperty;
    query->QueryType = PropertyStandardQuery;

    protocolData->ProtocolType = ProtocolTypeNvme;
    protocolData->DataType = NVMeDataTypeIdentify;
    protocolData->ProtocolDataRequestValue = NVME_IDENTIFY_CNS_CONTROLLER;
    protocolData->ProtocolDataRequestSubValue = 0;
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);
    protocolData->ProtocolDataLength = NVME_MAX_LOG_SIZE;

    //
    // Send request down.
    //
    result = DeviceIoControl(DeviceList[Index].Handle,
                             IOCTL_STORAGE_QUERY_PROPERTY,
                             buffer,
                             bufferLength,
                             buffer,
                             bufferLength,
                             &returnedLength,
                             NULL
                             );

    ZeroMemory(buffer, bufferLength);
    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < NVME_MAX_LOG_SIZE)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Identify Controller Data - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // Identify Controller Data 
    //
    {
        PNVME_IDENTIFY_CONTROLLER_DATA identifyControllerData = (PNVME_IDENTIFY_CONTROLLER_DATA)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        if ((identifyControllerData->VID == 0) ||
            (identifyControllerData->NN == 0)) {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Identify Controller Data not valid.\n"));
            goto exit;
        } else {
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: ***Identify Controller Data succeeded***.\n"));
        }
    }

  
```

> [!IMPORTANT]
> Para un [**IOCTL_STORAGE_QUERY_PROPERTY**](/windows/win32/api/winioctl/ni-winioctl-ioctl_storage_query_property) que usa un **STORAGE_PROPERTY_ID** de [**StorageAdapterProtocolSpecificProperty**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id)y cuya estructura [**STORAGE_PROTOCOL_SPECIFIC_DATA**](/windows/win32/api/winioctl/ns-winioctl-storage_protocol_specific_data) o [**STORAGE_PROTOCOL_SPECIFIC_DATA_EXT**](/windows-hardware/drivers/ddi/ntddstor/ns-ntddstor-storage_protocol_specific_data_ext) se establece en y , establezca el miembro ProtocolDataLength de esa misma estructura en un valor mínimo de `ProtocolType=ProtocolTypeNvme` `DataType=NVMeDataTypeLogPage` 512 (bytes).


Tenga en cuenta que el autor de la llamada debe asignar un solo búfer que contenga STORAGE PROPERTY QUERY y \_ el tamaño de STORAGE PROTOCOL SPECIFIC \_ \_ \_ \_ DATA. En este ejemplo, usa el mismo búfer para la entrada y salida de la consulta de propiedades. Por este motivo, el búfer asignado tiene un tamaño de "FIELD \_ OFFSET(STORAGE \_ PROPERTY \_ QUERY, AdditionalParameters) + sizeof(STORAGE \_ PROTOCOL SPECIFIC \_ \_ DATA) + NVME \_ MAX LOG \_ \_ SIZE". Aunque se podrían asignar búferes independientes para la entrada y la salida, se recomienda usar un solo búfer para consultar la información relacionada con NVMe.

### <a name="example-nvme-get-log-pages-query"></a>Ejemplo: Consulta de las páginas de registro get de NVMe

En este ejemplo, en función de la anterior, la solicitud **Obtener** páginas de registro se envía a una unidad NVMe. El código siguiente prepara la estructura de datos de consulta y, a continuación, envía el comando al dispositivo a través de DeviceIoControl.


```C++
    ZeroMemory(buffer, bufferLength);  

    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeLogPage;  
    protocolData->ProtocolDataRequestValue = NVME_LOG_PAGE_HEALTH_INFO;  
    protocolData->ProtocolDataRequestSubValue = 0;  // This will be passed as the lower 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue2 = 0; // This will be passed as the higher 32 bit of log page offset if controller supports extended data for the Get Log Page.
    protocolData->ProtocolDataRequestSubValue3 = 0; // This will be passed as Log Specific Identifier in CDW11.
    protocolData->ProtocolDataRequestSubValue4 = 0; // This will map to STORAGE_PROTOCOL_DATA_SUBVALUE_GET_LOG_PAGE definition, then user can pass Retain Asynchronous Event, Log Specific Field.

    protocolData->ProtocolDataOffset = sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA);  
    protocolData->ProtocolDataLength = sizeof(NVME_HEALTH_INFO_LOG);  

    //  
    // Send request down.  
    //  
    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer, 
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log failed. Error Code %d.\n"), GetLastError());
        goto exit;
    }

    //
    // Validate the returned data.
    //
    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - data descriptor header not valid.\n"));
        return;
    }

    protocolData = &protocolDataDescr->ProtocolSpecificData;

    if ((protocolData->ProtocolDataOffset < sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA)) ||
        (protocolData->ProtocolDataLength < sizeof(NVME_HEALTH_INFO_LOG))) {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log - ProtocolData Offset/Length not valid.\n"));
        goto exit;
    }

    //
    // SMART/Health Information Log Data 
    //
    {
        PNVME_HEALTH_INFO_LOG smartInfo = (PNVME_HEALTH_INFO_LOG)((PCHAR)protocolData + protocolData->ProtocolDataOffset);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: SMART/Health Information Log Data - Temperature %d.\n"), ((ULONG)smartInfo->Temperature[1] << 8 | smartInfo->Temperature[0]) - 273);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: ***SMART/Health Information Log succeeded***.\n"));
    }

```



### <a name="example-nvme-get-features-query"></a>Ejemplo: Consulta get features de NVMe

En este ejemplo, en función de la anterior, la solicitud **Obtener** características se envía a una unidad NVMe. El código siguiente prepara la estructura de datos de consulta y, a continuación, envía el comando al dispositivo a través de DeviceIoControl.


```C++
    //  
    // Initialize query data structure to Volatile Cache feature.  
    //  

    ZeroMemory(buffer, bufferLength);  


    query = (PSTORAGE_PROPERTY_QUERY)buffer;  
    protocolDataDescr = (PSTORAGE_PROTOCOL_DATA_DESCRIPTOR)buffer;  
    protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA)query->AdditionalParameters;  

    query->PropertyId = StorageDeviceProtocolSpecificProperty;  
    query->QueryType = PropertyStandardQuery;  

    protocolData->ProtocolType = ProtocolTypeNvme;  
    protocolData->DataType = NVMeDataTypeFeature;  
    protocolData->ProtocolDataRequestValue = NVME_FEATURE_VOLATILE_WRITE_CACHE;  
    protocolData->ProtocolDataRequestSubValue = 0;  
    protocolData->ProtocolDataOffset = 0;  
    protocolData->ProtocolDataLength = 0;  

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[Index].Handle,  
                             IOCTL_STORAGE_QUERY_PROPERTY,  
                             buffer,  
                             bufferLength,  
                             buffer,  
                             bufferLength,  
                             &returnedLength,  
                             NULL  
                             );  

    if (!result || (returnedLength == 0)) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache failed. Error Code %d.\n"), GetLastError());  
        goto exit;  
    }  

    //  
    // Validate the returned data.  
    //  

    if ((protocolDataDescr->Version != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR)) ||  
        (protocolDataDescr->Size != sizeof(STORAGE_PROTOCOL_DATA_DESCRIPTOR))) {  
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache  - data descriptor header not valid.\n"));  
        return;                                           
    }  

    //
    // Volatile Cache 
    //
    {
        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: Get Feature - Volatile Cache - %x.\n"), protocolDataDescr->ProtocolSpecificData.FixedProtocolReturnData);

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: ***Get Feature - Volatile Cache succeeded***.\n"));
    }
```
## <a name="protocol-specific-set"></a>Conjunto específico del protocolo

Desde Windows 10 19H1, el IOCTL_STORAGE_SET_PROPERTY se ha mejorado para admitir las características del conjunto nvme.

El búfer de entrada para el IOCTL_STORAGE_SET_PROPERTY se muestra aquí:

```C++
typedef struct _STORAGE_PROPERTY_SET {

    //
    // ID of the property being retrieved
    //

    STORAGE_PROPERTY_ID PropertyId;

    //
    // Flags indicating the type of set property being performed
    //

    STORAGE_SET_TYPE SetType;

    //
    // Space for additional parameters if necessary
    //

    UCHAR AdditionalParameters[1];

} STORAGE_PROPERTY_SET, *PSTORAGE_PROPERTY_SET;
```

Al usar IOCTL_STORAGE_SET_PROPERTY para establecer la característica NVMe, configure la STORAGE_PROPERTY_SET como se muestra a continuación:

-   Asigne un búfer que pueda contiene una estructura STORAGE_PROPERTY_SET y una STORAGE_PROTOCOL_SPECIFIC_DATA_EXT estructura;
-   Establezca el campo PropertyID en StorageAdapterProtocolSpecificProperty o StorageDeviceProtocolSpecificProperty para una solicitud de controlador o dispositivo o espacio de nombres, respectivamente.
-   Rellene la STORAGE_PROTOCOL_SPECIFIC_DATA_EXT estructura con los valores deseados. El inicio de la STORAGE_PROTOCOL_SPECIFIC_DATA_EXT es el campo AdditionalParameters de STORAGE_PROPERTY_SET.

La STORAGE_PROTOCOL_SPECIFIC_DATA_EXT estructura se muestra aquí.

```C++
typedef struct _STORAGE_PROTOCOL_SPECIFIC_DATA_EXT {

    STORAGE_PROTOCOL_TYPE ProtocolType;
    ULONG   DataType;                   // The value will be protocol specific, as defined in STORAGE_PROTOCOL_NVME_DATA_TYPE or STORAGE_PROTOCOL_ATA_DATA_TYPE.

    ULONG   ProtocolDataValue;
    ULONG   ProtocolDataSubValue;      // Data sub request value

    ULONG   ProtocolDataOffset;         // The offset of data buffer is from beginning of this data structure.
    ULONG   ProtocolDataLength;

    ULONG   FixedProtocolReturnData;
    ULONG   ProtocolDataSubValue2;     // First additional data sub request value

    ULONG   ProtocolDataSubValue3;     // Second additional data sub request value
    ULONG   ProtocolDataSubValue4;     // Third additional data sub request value

    ULONG   ProtocolDataSubValue5;     // Fourth additional data sub request value
    ULONG   Reserved[5];
} STORAGE_PROTOCOL_SPECIFIC_DATA_EXT, *PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT;
```

Para especificar un tipo de característica NVMe que se debe establecer, configure la STORAGE_PROTOCOL_SPECIFIC_DATA_EXT como se muestra a continuación:
-   Establezca el campo ProtocolType en ProtocolTypeNvme;
-   Establezca el campo DataType en el valor de enumeración NVMeDataTypeFeature definido por STORAGE_PROTOCOL_NVME_DATA_TYPE;

En los ejemplos siguientes se muestra el conjunto de características de NVMe.

### <a name="example-nvme-set-features"></a>Ejemplo: Características del conjunto de NVMe

En este ejemplo, la solicitud Establecer características se envía a una unidad NVMe. El código siguiente prepara la estructura de datos del conjunto y, a continuación, envía el comando al dispositivo a través de DeviceIoControl.

```C++
            PSTORAGE_PROPERTY_SET                   setProperty = NULL;
            PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT     protocolData = NULL;
            PSTORAGE_PROTOCOL_DATA_DESCRIPTOR_EXT   protocolDataDescr = NULL;

            //
            // Allocate buffer for use.
            //
            bufferLength = FIELD_OFFSET(STORAGE_PROPERTY_SET, AdditionalParameters) + sizeof(STORAGE_PROTOCOL_SPECIFIC_DATA_EXT);
            bufferLength += NVME_MAX_LOG_SIZE;

            buffer = new UCHAR[bufferLength];

            //
            // Initialize query data structure to get the desired log page.
            //
            ZeroMemory(buffer, bufferLength);

            setProperty = (PSTORAGE_PROPERTY_SET)buffer;

            setProperty->PropertyId = StorageAdapterProtocolSpecificProperty;
            setProperty->SetType = PropertyStandardSet;

            protocolData = (PSTORAGE_PROTOCOL_SPECIFIC_DATA_EXT)setProperty->AdditionalParameters;

            protocolData->ProtocolType = ProtocolTypeNvme;
            protocolData->DataType = NVMeDataTypeFeature;
            protocolData->ProtocolDataValue = NVME_FEATURE_HOST_CONTROLLED_THERMAL_MANAGEMENT;

            protocolData->ProtocolDataSubValue = 0; // This will pass to CDW11.
            protocolData->ProtocolDataSubValue2 = 0; // This will pass to CDW12.
            protocolData->ProtocolDataSubValue3 = 0; // This will pass to CDW13.
            protocolData->ProtocolDataSubValue4 = 0; // This will pass to CDW14.
            protocolData->ProtocolDataSubValue5 = 0; // This will pass to CDW15.

            protocolData->ProtocolDataOffset = 0;
            protocolData->ProtocolDataLength = 0;

            //
            // Send request down.
            //
            result = DeviceIoControl(m_deviceHandle,
                                     IOCTL_STORAGE_SET_PROPERTY,
                                     buffer,
                                     bufferLength,
                                     buffer,
                                     bufferLength,
                                     &returnedLength,
                                     NULL
            );
```

## <a name="temperature-queries"></a>Consultas de temperatura

En Windows 10, [**IOCTL \_ STORAGE \_ QUERY \_ PROPERTY**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) también se puede usar para consultar datos de temperatura desde dispositivos NVMe.

Para recuperar información de temperatura de una unidad NVMe en el [**\_ \_ \_ DESCRIPTOR DE**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor)DATOS DE TEMPERATURA DE ALMACENAMIENTO , configure la [**estructura STORAGE PROPERTY \_ \_ QUERY**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) de la siguiente manera:

-   Asigne un búfer que pueda contiene una [**estructura STORAGE \_ PROPERTY \_ QUERY.**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query)

-   Establezca el **campo PropertyID** en **StorageAdapterTemperatureProperty** o **StorageDeviceTemperatureProperty** para una solicitud de controlador o dispositivo o espacio de nombres, respectivamente.

-   Establezca el **campo QueryType** en **PropertyStandardQuery.**

La [**estructura STORAGE TEMPERATURE \_ \_ INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) (de Windows 10) se muestra aquí.


```C++
typedef struct _STORAGE_TEMPERATURE_INFO {

    USHORT  Index;                      // Starts from 0. Index 0 may indicate a composite value.
    SHORT   Temperature;                // Signed value; in Celsius.
    SHORT   OverThreshold;              // Signed value; in Celsius.
    SHORT   UnderThreshold;             // Signed value; in Celsius.

    BOOLEAN OverThresholdChangable;     // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN UnderThresholdChangable;    // Can the threshold value being changed by using IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD.
    BOOLEAN EventGenerated;             // Indicates that notification will be generated when temperature cross threshold.
    UCHAR   Reserved0;
    ULONG   Reserved1;

} STORAGE_TEMPERATURE_INFO, *PSTORAGE_TEMPERATURE_INFO;
```



## <a name="behavior-changing-commands"></a>Comandos de cambio de comportamiento

Los comandos que manipulan atributos de dispositivo o que pueden afectar al comportamiento del dispositivo son más difíciles de tratar para el sistema operativo. Si los atributos del dispositivo cambian en tiempo de ejecución mientras se procesa la E/S, pueden surgir problemas de sincronización o integridad de datos si no se controlan correctamente.

El comando **NvMe Set-Features** es un buen ejemplo de un comando de cambio de comportamiento. Permite cambiar el mecanismo de conciliación y la configuración de umbrales de temperatura. Para asegurarse de que los datos en marcha no están en riesgo cuando se envían comandos set que afectan al comportamiento, Windows pausará todas las E/S en el dispositivo NVMe, purgará las colas y vaciará los búferes. Una vez que el comando set se ha ejecutado correctamente, se reanuda la E/S (si es posible). Si no se puede reanudar la E/S, puede ser necesario restablecer el dispositivo.

### <a name="setting-temperature-thresholds"></a>Establecimiento de umbrales de temperatura

Windows 10 el UMBRAL DE TEMPERATURA DEL CONJUNTO DE ALMACENAMIENTO DE [**IOCTL, \_ \_ \_ \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold)una IOCTL para obtener y establecer umbrales de temperatura. También puede usarlo para obtener la temperatura actual del dispositivo. El búfer de entrada/salida de esta IOCTL es la estructura [**STORAGE \_ TEMPERATURE \_ INFO**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) de la sección de código anterior.

### <a name="example-setting-over-threshold-temperature"></a>Ejemplo: Establecimiento de la temperatura por encima del umbral

En este ejemplo, se establece la temperatura por encima del umbral de una unidad NVMe. El código siguiente prepara el comando y, a continuación, lo envía al dispositivo a través de DeviceIoControl.


```C++
    BOOL    result;  
    ULONG   returnedLength = 0;  
    
    STORAGE_TEMPERATURE_THRESHOLD setThreshold = {0};  

    setThreshold.Version = sizeof(STORAGE_TEMPERATURE_THRESHOLD); 
    setThreshold.Size = sizeof(STORAGE_TEMPERATURE_THRESHOLD);  
    setThreshold.Flags = STORAGE_TEMPERATURE_THRESHOLD_FLAG_ADAPTER_REQUEST;  
    setThreshold.Index = SensorIndex;  
    setThreshold.Threshold = Threshold;  
    setThreshold.OverThreshold = UpdateOverThreshold; 

    //  
    // Send request down.  
    //  

    result = DeviceIoControl(DeviceList[DeviceIndex].Handle,  
                             IOCTL_STORAGE_SET_TEMPERATURE_THRESHOLD,  
                             &setThreshold,  
                             sizeof(STORAGE_TEMPERATURE_THRESHOLD),  
                             NULL,  
                             0,  
                             &returnedLength,  
                             NULL  
                             ); 

```



### <a name="setting-vendor-specific-features"></a>Configuración de características específicas del proveedor

Sin el registro de efectos de comando, el controlador no tiene conocimiento de las ramificaciones del comando. Este es el motivo por el que se requiere el registro de efectos de comando. Ayuda al sistema operativo a determinar si un comando tiene un gran impacto y si se puede enviar en paralelo con otros comandos a la unidad.

El registro de efectos de comando aún no es lo suficientemente granular como para abarcar comandos **Set-Features** específicos del proveedor. Por esta razón, todavía no es posible enviar comandos **Set-Features** específicos del proveedor. Sin embargo, es posible usar el mecanismo de paso a través, que se ha mencionado anteriormente, para enviar comandos específicos del proveedor. Para obtener más información, vea [Mecanismo de paso a través](#pass-through-mechanism).

## <a name="header-files"></a>Archivos de encabezado

Los siguientes archivos son relevantes para el desarrollo de NVMe. Estos archivos se incluyen con el Kit [de desarrollo Windows software (SDK) de Microsoft.](https://developer.microsoft.com/windows/downloads)



| Archivo de encabezado    | Descripción                                                                             |
|----------------|-----------------------------------------------------------------------------------------|
| **ntddstor.h** | Define constantes y tipos para acceder a los controladores de clase de almacenamiento desde el modo kernel.   |
| **nvme.h**     | Para otras estructuras de datos relacionadas con NVMe.                                                 |
| **winioctl.h** | Para las definiciones de IOCTL de Win32 generales, incluidas las API de almacenamiento para las aplicaciones en modo de usuario. |



 

 

 
