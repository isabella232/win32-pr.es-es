---
description: Obtenga información sobre cómo trabajar con dispositivos de NVMe de alta velocidad desde la aplicación Windows.
ms.assetid: 037AF841-C2C9-4551-9CCB-F2A2F199083A
title: Trabajar con unidades de NVMe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9be94adf8355940bd93de137d122d91e468c2173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666818"
---
# <a name="working-with-nvme-drives"></a>Trabajar con unidades de NVMe

**Se aplica a:**

-   Windows 10
-   Windows Server 2016

Obtenga información sobre cómo trabajar con dispositivos de NVMe de alta velocidad desde la aplicación Windows. El acceso al dispositivo se habilita a través de **StorNVMe.sys**, el controlador incluido por primera vez en Windows Server 2012 R2 y Windows 8.1. También está disponible para los dispositivos de Windows 7 a través de una corrección urgente de KB. En Windows 10, se introdujeron varias características nuevas, incluido un mecanismo de paso a través para comandos de NVMe específicos del proveedor y actualizaciones de los ioctl existentes.

En este tema se proporciona información general sobre las API de uso general que puede usar para tener acceso a las unidades de NVMe en Windows 10. También se describe:

-   Cómo enviar un comando de NVMe específico del proveedor con [paso a través](#pass-through-mechanism)
-   Cómo [Enviar un comando de identificación, obtener características u obtener páginas de registro](#protocol-specific-queries) a la unidad de NVMe
-   Obtención de [información de temperatura](#temperature-queries) de una unidad de NVMe
-   Realización de comandos de cambio de comportamiento, como el [establecimiento de umbrales de temperatura](#behavior-changing-commands)

## <a name="apis-for-working-with-nvme-drives"></a>API para trabajar con unidades de NVMe

Puede usar las siguientes API de uso general para acceder a las unidades de NVMe en Windows 10. Estas API se pueden encontrar en **winioctl. h** para las aplicaciones en modo de usuario y **ntddstor. h** para los controladores en modo kernel. Para obtener más información acerca de los archivos de encabezado, consulte [archivos de encabezado](#header-files).

-   [**Ioctl \_ \_ \_ Comando de protocolo de almacenamiento**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command) : Use este ioctl con la estructura de **\_ \_ comandos del Protocolo de almacenamiento** para emitir comandos de NVMe. Este IOCTL permite el paso a través de NVMe y admite el registro de efectos de comando en NVMe. Puede usarlo con comandos específicos del proveedor. Para obtener más información, vea [mecanismo de paso a través](#pass-through-mechanism).

-   [**Almacenamiento \_ de \_Comando de protocolo**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) : esta estructura de búfer de entrada incluye un campo **ReturnStatus** que se puede usar para notificar los siguientes valores de estado.
    -   **Estado del Protocolo de almacenamiento \_ \_ \_ pendiente**
    -   **Estado del Protocolo de almacenamiento \_ \_ \_ correcta**
    -   **\_error de \_ Estado del Protocolo de almacenamiento \_**
    -   **Estado del Protocolo de almacenamiento \_ \_ \_ solicitud no válida \_**
    -   **Estado del Protocolo de almacenamiento \_ \_ \_ sin \_ dispositivo**
    -   **Estado de protocolo de almacenamiento \_ \_ \_ ocupado**
    -   **\_saturación de \_ datos de estado del Protocolo de almacenamiento \_ \_**
    -   **\_ \_ \_ faltan recursos en el estado del Protocolo de almacenamiento \_**
    -   **Estado del Protocolo de almacenamiento \_ \_ \_ no \_ admitido**
-   [**Ioctl \_ \_ \_ Propiedad de consulta de almacenamiento**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) : Use este ioctl con la estructura de la **\_ \_ consulta de propiedades de almacenamiento** para recuperar la información del dispositivo. Para obtener más información, consulte consultas [específicas del protocolo](#protocol-specific-queries) y [consultas de temperatura](#temperature-queries).

-   [**Almacenamiento \_ de \_Consulta de propiedad**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) : esta estructura incluye los campos **PropertyId** y **AdditionalParameters** para especificar los datos que se van a consultar. En **PropertyId** , utilice la enumeración **\_ \_ ID** . de propiedad de almacenamiento para especificar el tipo de datos. Use el campo **AdditionalParameters** para especificar más detalles, dependiendo del tipo de datos. En el caso de los datos específicos del Protocolo, use la estructura de **\_ \_ \_ datos específica del Protocolo de almacenamiento** en el campo **AdditionalParameters** . Para los datos de temperatura, use la estructura de **\_ \_ información de temperatura de almacenamiento** en el campo **AdditionalParameters** .
-   [**Almacenamiento \_ de \_ID. de propiedad**](/windows/win32/api/winioctl/ne-winioctl-storage_property_id) : esta enumeración incluye nuevos valores que permiten que la **\_ \_ \_ propiedad de consulta de almacenamiento ioctl** recupere información específica del protocolo y de la temperatura.

    -   **StorageAdapterProtocolSpecificProperty**
    -   **StorageDeviceProtocolSpecificProperty**

    Use uno de estos identificadores de propiedad específicos del protocolo en combinación con **\_ \_ \_ datos específicos del Protocolo de almacenamiento** para recuperar datos específicos del protocolo en la estructura de [**\_ \_ \_ descriptor de datos del Protocolo de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor) .

    -   **StorageAdapterTemperatureProperty**
    -   **StorageDeviceTemperatureProperty**

    Use uno de estos identificadores de propiedad de temperatura para recuperar los datos de temperatura en la estructura de [**\_ \_ \_ descriptor de datos de temperatura de almacenamiento**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor) .

-   [**Almacenamiento \_ de \_ \_ Datos específicos del protocolo**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) : Recupere datos específicos de NVMe cuando esta estructura se usa para el campo **AdditionalParameters** de la consulta de **\_ propiedades \_ de almacenamiento** y se especifica un valor de enumeración de [**tipo de datos de nVMe del Protocolo de almacenamiento \_ \_ \_ \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type) . Use uno de los siguientes valores de **tipo de datos de protocolo de almacenamiento \_ \_ NVME \_ \_** en el campo **DataType** de la estructura de **\_ \_ \_ datos específica del Protocolo de almacenamiento** :

    -   Use **NVMeDataTypeIdentify** para obtener los datos del controlador de identificación o identificar los datos del espacio de nombres.
    -   Use **NVMeDataTypeLogPage** para obtener páginas de registro (incluidos los datos de estado o inteligentes).
    -   Use **NVMeDataTypeFeature** para obtener características de la unidad de NVMe.

-   [**Almacenamiento \_ de \_Información de temperatura**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) : esta estructura se usa para almacenar datos de temperatura concretos. Se usa en el **\_ \_ \_ descriptor de datos TEMERATURE de almacenamiento** para devolver los resultados de una consulta de temperatura.

-   [**Ioctl \_ \_Umbral de \_ temperatura \_ del conjunto de almacenamiento**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold) : Use este ioctl con la estructura del **\_ \_ umbral de temperatura de almacenamiento** para establecer los umbrales de temperatura. Para obtener más información, consulte [Behavior Changing Commands](#behavior-changing-commands).

-   [**Almacenamiento \_ de \_Umbral de temperatura**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_threshold) : esta estructura se usa como búfer de entrada para especificar el umbral de temperatura. El campo de **sobreumbral** (booleano) especifica si el campo de **umbral** es el valor de umbral superior o no (de lo contrario, es el valor de umbral inferior).

## <a name="pass-through-mechanism"></a>Mecanismo de paso a través

Los comandos que no están definidos en la especificación de NVMe son los más difíciles de controlar para el SO del host: el host no tiene información sobre los efectos que pueden tener los comandos en el dispositivo de destino, la infraestructura expuesta (tamaños de espacios de nombres y bloques) y su comportamiento.

Para realizar mejor los comandos específicos de este dispositivo a través de la pila de almacenamiento de Windows, un nuevo mecanismo de paso permite canalizar comandos específicos del proveedor. Esta canalización de paso a través también ayudará en el desarrollo de herramientas de administración y pruebas. Sin embargo, este mecanismo de paso a través requiere el uso del registro de efectos de comando. Además, StoreNVMe.sys requiere que todos los comandos, no solo los comandos de paso a través, se describirán en el registro de efectos de comando.

> [!IMPORTANT]
> StorNVMe.sys y Storport.sys bloquearán cualquier comando en un dispositivo si no se describe en el registro de efectos de comandos.

 

### <a name="supporting-the-command-effects-log"></a>Compatibilidad con el registro de efectos de comando

El registro de efectos de comando (como se describe en comandos compatibles y efectos, sección 5.10.1.5 de la [especificación de NVMe 1,2](https://nvmexpress.org/specifications)) permite la descripción de los efectos de los comandos específicos del proveedor junto con los comandos definidos por la especificación. Esto facilita la validación de la compatibilidad de comandos, así como la optimización del comportamiento del comando y, por lo tanto, debe implementarse para todo el conjunto de comandos que admite el dispositivo. Las siguientes condiciones describen el resultado de cómo se envía el comando en función de su entrada de registro de efectos de comando.

Para cualquier comando específico descrito en el registro de efectos de comandos...

**While**:

-   El comando compatible (CSUPP) se establece en ' 1 ', lo que significa que el comando es compatible con el controlador (bit 01)

    > [!Note]  
    > Cuando CSUPP se establece en "0" (lo que significa que no se admite el comando), se bloqueará el comando.

     

**Y si** se establece alguna de las siguientes opciones:

-   El cambio de capacidad del controlador (CCC) se establece en ' 1 ', lo que significa que el comando puede cambiar las capacidades del controlador (bit 04)

-   El cambio de inventario de espacios de nombres (NIC) se establece en ' 1 ', lo que significa que el comando puede cambiar el número o capacidades para varios espacios de nombres (bit 03)

-   El cambio de capacidad de espacio de nombres (NCC) se establece en ' 1 ', lo que significa que el comando puede cambiar las capacidades de un solo espacio de nombres (bit 02)

-   El envío y la ejecución de comandos (CSE) se establece en 001B o 010B, lo que significa que el comando se puede enviar cuando no hay ningún otro comando pendiente al mismo espacio de nombres o a cualquier otro comando, y que no se debe enviar otro comando al mismo espacio de nombres o a cualquier otro espacio de nombres hasta que se complete este comando (bits 18:16)

**A continuación,** el comando se enviará como el único comando pendiente del adaptador.

De lo **contrario, si**:

-   El envío y la ejecución de comandos (CSE) se establecen en 001B, lo que significa que el comando se puede enviar cuando no hay ningún otro comando pendiente al mismo espacio de nombres y que no se debe enviar otro comando al mismo espacio de nombres hasta que se complete este comando (bits 18:16)

**A continuación,** el comando se enviará como el único comando pendiente al objeto de número de unidad lógica (LUN).

De **lo contrario**, el comando se envía con otros comandos pendientes sin inhibición. Por ejemplo, si se envía un comando específico del proveedor al dispositivo para recuperar información estadística no definida por la especificación, no debería haber ningún riesgo de cambiar el comportamiento del dispositivo o la capacidad de ejecutar comandos de e/s. Estas solicitudes se pueden atender en paralelo a e/s y no sería necesario pausar PAUSE-resume.

### <a name="using-ioctl_storage_protocol_command-to-send-commands"></a>Uso del \_ \_ \_ comando de protocolo de almacenamiento ioctl para enviar comandos

El paso a través se puede realizar mediante [**el \_ \_ \_ comando de protocolo de almacenamiento ioctl**](/windows/desktop/api/winioctl/ni-winioctl-ioctl_storage_protocol_command), introducido en Windows 10. Este IOCTL se diseñó para tener un comportamiento similar al de los ioctl de paso a través de SCSI y ATA existentes, a fin de enviar un comando incrustado al dispositivo de destino. A través de este IOCTL, el paso a través se puede enviar a un dispositivo de almacenamiento, incluida una unidad de NVMe.

Por ejemplo, en NVMe, IOCTL permitirá el envío de los siguientes códigos de comando.

-   Comandos de administración específicos del proveedor (C0h – FFh)
-   Comandos de NVMe específicos del proveedor (80h – FFh)

Como con todos los demás ioctl, use [**DeviceIoControl**](/windows/desktop/api/ioapiset/nf-ioapiset-deviceiocontrol) para enviar el ioctl de paso a través. El IOCTL se rellena mediante la estructura de búfer de entrada del [**\_ \_ comando del Protocolo de almacenamiento**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) que se encuentra en **ntddstor. h**. Rellene el campo **comando** con el comando específico del proveedor.


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



El comando específico del proveedor que se desea enviar se debe rellenar en el campo resaltado anterior. Vuelva a tener en cuenta que el registro de efectos de comando debe implementarse para los comandos de paso a través. En concreto, estos comandos deben aparecer como compatibles en el registro de efectos de comando (consulte la sección anterior para obtener más información). Tenga en cuenta también que los campos PRP son específicos del controlador, por lo que las aplicaciones que envían comandos pueden dejarlos como 0.

Por último, este IOCTL de paso a través está pensado para enviar comandos específicos del proveedor. No se debe usar este IOCTL de paso a través para enviar otros comandos de NVMe específicos de administrador o no de proveedor, como la identificación. Por ejemplo, **la \_ \_ \_ propiedad consulta de almacenamiento ioctl** debe usarse para identificar o obtener páginas de registro. Para obtener más información, vea la sección siguiente, [consultas específicas del protocolo](/windows).

### <a name="dont-update-firmware-through-the-pass-through-mechanism"></a>No actualice el firmware a través del mecanismo de paso a través

Los comandos de descarga y activación del firmware no se deben enviar mediante el paso a través. **Ioctl \_ El \_ \_ comando de protocolo de almacenamiento** solo se debe usar para comandos específicos del proveedor.

En su lugar, use los siguientes ioctl de almacenamiento general (introducidos en Windows 10) para evitar que las aplicaciones usen directamente la \_ versión de MINIPUERTO SCSI del ioctl de firmware. Los controladores de almacenamiento traducirán el IOCTL a un comando SCSI o a la \_ versión del MINIPUERTO SCSI del ioctl en el minipuerto.

Estos ioctl se recomiendan para desarrollar herramientas de actualización de firmware en Windows 10 y Windows Server 2016:

-   [**\_ \_ \_ obtener información de firmware de almacenamiento de ioctl \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_get_info)
-   [**\_descarga de \_ firmware de almacenamiento de ioctl \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_download)
-   [**\_ \_ Activar firmware de almacenamiento de ioctl \_**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_firmware_activate)

Para obtener información de almacenamiento y actualizar el firmware, Windows también admite cmdlets de PowerShell para hacerlo rápidamente:

-   `Get-StorageFirmwareInfo`
-   `Update-StorageFirmware `

> [!Note]  
> Para actualizar el firmware en NVMe en Windows 8.1, use \_ el \_ firmware del minipuerto SCSI de ioctl \_ . Este IOCTL no se ha trasladado a Windows 7. Para obtener más información, consulte [actualización del firmware de un dispositivo de NVMe en Windows 8.1](/windows-hardware/drivers/storage/upgrading-firmware-for-an-nvme-device).

 

### <a name="returning-errors-through-the-pass-through-mechanism"></a>Devolver errores a través del mecanismo de paso a través

Similar a los ioctl de paso a través de SCSI y ATA, cuando se envía un comando o una solicitud al minipuerto o dispositivo, el IOCTL devuelve si es correcto o no. En la estructura de [**\_ \_ comandos del Protocolo de almacenamiento**](/windows/desktop/api/winioctl/ns-winioctl-storage_protocol_command) , el ioctl devuelve el estado a través del campo **ReturnStatus** .

### <a name="example-sending-a-vendor-specific-command"></a>Ejemplo: enviar un comando específico del proveedor

En este ejemplo, se envía un comando específico del proveedor (0xFF) arbitrario a través de un paso a una unidad de NVMe. El código siguiente asigna un búfer, Inicializa una consulta y, a continuación, envía el comando al dispositivo a través de DeviceIoControl.


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



En este ejemplo, se espera `protocolCommand->ReturnStatus == STORAGE_PROTOCOL_STATUS_SUCCESS` que el comando se haya ejecutado correctamente en el dispositivo.

## <a name="protocol-specific-queries"></a>Consultas específicas del Protocolo

Windows 8.1 ha introducido la [**\_ propiedad de \_ consulta \_ de almacenamiento ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) para la recuperación de datos. En Windows 10, el IOCTL se mejoró para admitir las características de NVMe solicitadas comúnmente, como **obtener páginas de registro**, **obtener características** e **identificar**. Esto permite la recuperación de información específica de NVMe para fines de supervisión e inventario.

Aquí se muestra el búfer de entrada de IOCTL, la [**\_ \_ consulta de propiedades de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) (desde Windows 10).


```C++
typedef struct _STORAGE_PROPERTY_QUERY {
    STORAGE_PROPERTY_ID PropertyId;
    STORAGE_QUERY_TYPE QueryType;
    UCHAR  AdditionalParameters[1];
} STORAGE_PROPERTY_QUERY, *PSTORAGE_PROPERTY_QUERY;
```



Al utilizar [**la \_ \_ \_ propiedad de consulta de almacenamiento ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) para recuperar información específica del Protocolo de NVMe en el [**\_ \_ \_ descriptor de datos del Protocolo de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_data_descriptor), configure la estructura de [**\_ \_ consulta de propiedades de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) de la siguiente manera:

-   Asigna un búfer que puede contener una [**consulta de \_ propiedades \_ de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) y una estructura de [**\_ \_ \_ datos específica del Protocolo de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) .

-   Establezca el campo **PropertyID** en **StorageAdapterProtocolSpecificProperty** o **StorageDeviceProtocolSpecificProperty** para una solicitud de controlador o dispositivo/espacio de nombres, respectivamente.

-   Establezca el campo **QueryType** en **PropertyStandardQuery**.

-   Rellene la estructura de [**\_ \_ \_ datos específica del Protocolo de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) con los valores deseados. El inicio de los **\_ \_ \_ datos específicos del Protocolo de almacenamiento** es el campo **AdditionalParameters** de la consulta de la [**\_ propiedad \_ Storage**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query).

Aquí se muestra la estructura de [**\_ \_ \_ datos específica del Protocolo de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) (de Windows 10).


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



Para especificar un tipo de información específica del Protocolo de NVMe, configure la estructura de [**\_ \_ \_ datos específica del Protocolo de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_protocol_specific_data) de la siguiente manera:

-   Establezca el campo **protocolType** en **ProtocolTypeNVMe**.

-   Establezca el campo **DataType** en un valor de enumeración definido por el tipo de [**datos de protocolo de almacenamiento \_ \_ NVME \_ \_**](/windows/desktop/api/WinIoCtl/ne-winioctl-storage_protocol_nvme_data_type):

    -   Use **NVMeDataTypeIdentify** para obtener los datos del controlador de identificación o identificar los datos del espacio de nombres.
    -   Use **NVMeDataTypeLogPage** para obtener páginas de registro (incluidos los datos de estado o inteligentes).
    -   Use **NVMeDataTypeFeature** para obtener características de la unidad de NVMe.

Cuando se usa **ProtocolTypeNVMe** como **protocolType**, las consultas de información específica del Protocolo se pueden recuperar en paralelo con otras e/s en la unidad de NVMe.

En los siguientes ejemplos se muestran las consultas específicas del protocolo NVMe.

### <a name="example-nvme-identify-query"></a>Ejemplo: la consulta de identificación de NVMe

En este ejemplo, la solicitud de **identificación** se envía a una unidad de NVMe. El código siguiente inicializa la estructura de datos de consulta y, a continuación, envía el comando al dispositivo a través de DeviceIoControl.


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
            _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Identify Controller Data succeeded_*_.\n"));
        }
    }

  
```



Tenga en cuenta que el autor de la llamada debe asignar un único búfer que contiene \_ \_ la consulta de propiedades de almacenamiento y el tamaño de los \_ datos específicos del Protocolo de almacenamiento \_ \_ . En este ejemplo, se usa el mismo búfer para la entrada y la salida de la consulta de propiedad. Esta es la razón por la que el búfer asignado tiene un tamaño de "desplazamiento de campo \_ ( \_ consulta de propiedad \_ de almacenamiento, AdditionalParameters) + sizeof ( \_ \_ datos específicos del Protocolo de almacenamiento \_ ) + NVME ( \_ tamaño máximo de registro) \_ \_ ". Aunque se podrían asignar búferes independientes para la entrada y la salida, se recomienda usar un solo búfer para consultar información relacionada con NVMe.

### <a name="example-nvme-get-log-pages-query"></a>Ejemplo: consulta de las páginas de registro de NVMe

En este ejemplo, basado en el anterior, la solicitud _ *Get log pages** se envía a una unidad de NVMe. En el código siguiente se prepara la estructura de datos de consulta y, a continuación, se envía el comando al dispositivo a través de DeviceIoControl.


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

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_SMART/Health Information Log succeeded_*_.\n"));
    }

```



### <a name="example-nvme-get-features-query"></a>Ejemplo: consulta de funciones de búsqueda de NVMe

En este ejemplo, basado en el anterior, la solicitud _ *Get Features** se envía a una unidad de NVMe. En el código siguiente se prepara la estructura de datos de consulta y, a continuación, se envía el comando al dispositivo a través de DeviceIoControl.


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

        _tprintf(_T("DeviceNVMeQueryProtocolDataTest: **_Get Feature - Volatile Cache succeeded_*_.\n"));
    }
```
## <a name="protocol-specific-set"></a>Conjunto específico del Protocolo

En Windows 10 19H1, el IOCTL_STORAGE_SET_PROPERTY se mejoró para admitir las características del conjunto de NVMe.

El búfer de entrada del IOCTL_STORAGE_SET_PROPERTY se muestra aquí:

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

} STORAGE_PROPERTY_SET, _PSTORAGE_PROPERTY_SET;
```

Al usar IOCTL_STORAGE_SET_PROPERTY para establecer la característica de NVMe, configure la estructura de STORAGE_PROPERTY_SET como se indica a continuación:

-   Asigna un búfer que puede contener un STORAGE_PROPERTY_SET y una estructura de STORAGE_PROTOCOL_SPECIFIC_DATA_EXT;
-   Establezca el campo PropertyID en StorageAdapterProtocolSpecificProperty o StorageDeviceProtocolSpecificProperty para una solicitud de controlador o dispositivo/espacio de nombres, respectivamente.
-   Rellene la estructura de STORAGE_PROTOCOL_SPECIFIC_DATA_EXT con los valores deseados. El inicio del STORAGE_PROTOCOL_SPECIFIC_DATA_EXT es el campo AdditionalParameters de STORAGE_PROPERTY_SET.

Aquí se muestra la estructura de STORAGE_PROTOCOL_SPECIFIC_DATA_EXT.

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

Para especificar un tipo de característica de NVMe que se va a establecer, configure la STORAGE_PROTOCOL_SPECIFIC_DATA_EXT estructura de la siguiente manera:
-   Establezca el campo ProtocolType en ProtocolTypeNvme;
-   Establezca el campo DataType en el valor de enumeración NVMeDataTypeFeature definido por STORAGE_PROTOCOL_NVME_DATA_TYPE;

En los siguientes ejemplos se muestra el conjunto de características de NVMe.

### <a name="example-nvme-set-features"></a>Ejemplo: características del conjunto de NVMe

En este ejemplo, la solicitud Set Features se envía a una unidad de NVMe. En el código siguiente se prepara la estructura de datos establecida y, a continuación, se envía el comando al dispositivo a través de DeviceIoControl.

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

En Windows 10, [**la \_ \_ \_ propiedad consulta de almacenamiento de ioctl**](/windows/desktop/api/WinIoCtl/ni-winioctl-ioctl_storage_query_property) también se puede usar para consultar datos de temperatura de los dispositivos NVMe.

Para recuperar información de temperatura de una unidad de NVMe en el [**\_ \_ \_ descriptor de datos de temperatura de almacenamiento**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_data_descriptor), configure la estructura de [**\_ \_ consulta de propiedades de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) de la siguiente manera:

-   Asigna un búfer que puede contener una estructura de [**\_ \_ consulta de propiedades de almacenamiento**](/windows/desktop/api/WinIoCtl/ns-winioctl-storage_property_query) .

-   Establezca el campo **PropertyID** en **StorageAdapterTemperatureProperty** o **StorageDeviceTemperatureProperty** para una solicitud de controlador o dispositivo/espacio de nombres, respectivamente.

-   Establezca el campo **QueryType** en **PropertyStandardQuery**.

Aquí se muestra la estructura de [**\_ \_ información de temperatura de almacenamiento**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) (desde Windows 10).


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

Los comandos que manipulan atributos de dispositivo o que pueden afectar al comportamiento del dispositivo son más difíciles de tratar con el sistema operativo. Si los atributos del dispositivo cambian en tiempo de ejecución mientras se procesan las operaciones de e/s, pueden surgir problemas de integridad de datos o de sincronización si no se administran correctamente.

El comando **set-Features** de NVMe es un buen ejemplo de un comando de cambio de comportamiento. Permite cambiar el mecanismo de arbitraje y la configuración de umbrales de temperatura. Para asegurarse de que los datos en vuelo no estén en riesgo cuando se envíen los comandos SET que afectan al comportamiento, Windows pausará todas las e/s en el dispositivo de NVMe, las colas de purga y los búferes de vaciado. Una vez que el comando set se ha ejecutado correctamente, se reanuda la e/s (si es posible). Si no se puede reanudar la e/s, puede que sea necesario restablecer el dispositivo.

### <a name="setting-temperature-thresholds"></a>Configuración de umbrales de temperatura

Windows 10 presentó [**el \_ \_ umbral de \_ temperatura \_ del conjunto de almacenamiento ioctl**](/windows/desktop/api/WinIoctl/ni-winioctl-ioctl_storage_set_temperature_threshold), un ioctl para obtener y establecer umbrales de temperatura. También puede usarlo para obtener la temperatura actual del dispositivo. El búfer de entrada y salida para este IOCTL es la estructura de [**\_ \_ información de temperatura de almacenamiento**](/windows/desktop/api/WinIoctl/ns-winioctl-storage_temperature_info) , de la sección de código anterior.

### <a name="example-setting-over-threshold-temperature"></a>Ejemplo: establecer la temperatura supera el umbral

En este ejemplo, se establece la temperatura super del umbral de la unidad de NVMe. El código siguiente prepara el comando y, a continuación, lo envía al dispositivo a través de DeviceIoControl.


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

El registro de efectos de comando todavía no es suficientemente granular para abarcar los comandos **set-Features** específicos del proveedor. Por esta razón, todavía no es posible enviar comandos **set-Features** específicos del proveedor. Sin embargo, es posible usar el mecanismo de paso a través, descrito anteriormente, para enviar comandos específicos del proveedor. Para obtener más información, vea [mecanismo de paso a través](#pass-through-mechanism).

## <a name="header-files"></a>Archivos de encabezado

Los siguientes archivos son relevantes para el desarrollo de NVMe. Estos archivos se incluyen en el [Kit de desarrollo de software (SDK) de Microsoft Windows](https://developer.microsoft.com/windows/downloads).



| Archivo de encabezado    | Descripción                                                                             |
|----------------|-----------------------------------------------------------------------------------------|
| **ntddstor. h** | Define constantes y tipos para tener acceso a los controladores de clase de almacenamiento desde el modo kernel.   |
| **nVMe. h**     | Para otras estructuras de datos relacionadas con NVMe.                                                 |
| **winioctl. h** | Para las definiciones de IOCTL de Win32 generales, incluidas las API de almacenamiento para aplicaciones de modo de usuario. |



 

 

 
