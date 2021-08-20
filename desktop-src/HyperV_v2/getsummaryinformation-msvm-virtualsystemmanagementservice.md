---
description: Devuelve información de resumen de la máquina virtual.
ms.assetid: CDDC2B5A-8172-4E6D-A206-CEAB9E54C69A
title: Método GetSummaryInformation de la Msvm_VirtualSystemManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: efa879cd3da0f5e8a4cc8cf1e9873390c94a94bae0eef3dd8d36c59c9e1680e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119253655"
---
# <a name="getsummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método GetSummaryInformation de la clase Msvm \_ VirtualSystemManagementService

Devuelve información de resumen de la máquina virtual.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetSummaryInformation(
  [in]  CIM_VirtualSystemSettingData REF SettingData[],
  [in]  uint32                           RequestedInformation[],
  [out] Msvm_SummaryInformationBase      SummaryInformation[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SettingData* \[ En\]
</dt> <dd>

Tipo: **CIM \_ \[ \] VirtualSystemSettingData**

Matriz de [**instancias de CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85)) que especifican las máquinas virtuales o instantáneas para las que se va a recuperar información. Si este parámetro es **Null,** se recupera la información de todas las máquinas virtuales.

</dd> <dt>

*RequestedInformation* \[ En\]
</dt> <dd>

Tipo: **uint32 \[ \]**

Matriz de valores de enumeración, que corresponden a las propiedades de la clase [**Msvm \_ SummaryInformation,**](msvm-summaryinformation.md) que especifican los datos que se recuperarán para las máquinas virtuales y las instantáneas especificadas en la matriz *SettingData.*

<dt>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>

<span id="Name"></span><span id="name"></span><span id="NAME"></span>**Nombre** (0)


</dt> <dd>

Esto corresponde a la **propiedad Name** de la [**clase \_ SummaryInformation de Msvm.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>

<span id="Element_Name"></span><span id="element_name"></span><span id="ELEMENT_NAME"></span>**Nombre del elemento** (1)


</dt> <dd>

Esto corresponde a la **propiedad ElementName** de la [**clase \_ SummaryInformation de Msvm.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>

<span id="Creation_Time"></span><span id="creation_time"></span><span id="CREATION_TIME"></span>**Hora de creación** (2)


</dt> <dd>

Esto corresponde a la **propiedad CreationTime** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>

<span id="Notes"></span><span id="notes"></span><span id="NOTES"></span>**Notas** (3)


</dt> <dd>

Esto corresponde a la **propiedad Notes** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>

<span id="Number_of_Processors"></span><span id="number_of_processors"></span><span id="NUMBER_OF_PROCESSORS"></span>**Número de procesadores** (4)


</dt> <dd>

Esto corresponde a la **propiedad NumberOfProcessors** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>

<span id="Small_Thumbnail_Image__80x60_"></span><span id="small_thumbnail_image__80x60_"></span><span id="SMALL_THUMBNAIL_IMAGE__80X60_"></span>**Imagen en miniatura pequeña (80 x 60)** (5)


</dt> <dd>

Esto corresponde a la **propiedad ThumbnailImage** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md) Se recuperará una imagen en miniatura con las dimensiones de 80 60.

</dd> <dt>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>

<span id="Medium_Thumbnail_Image__160x120_"></span><span id="medium_thumbnail_image__160x120_"></span><span id="MEDIUM_THUMBNAIL_IMAGE__160X120_"></span>**Imagen de miniatura media (160 x 120)** (6)


</dt> <dd>

Esto corresponde a la **propiedad ThumbnailImage** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md) Se recuperará una imagen en miniatura con las dimensiones de 160 120.

</dd> <dt>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>

<span id="Large_Thumbnail_Image__320x240_"></span><span id="large_thumbnail_image__320x240_"></span><span id="LARGE_THUMBNAIL_IMAGE__320X240_"></span>**Imagen de miniatura grande (320 x 240)** (7)


</dt> <dd>

Esto corresponde a la **propiedad ThumbnailImage** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md) Se recuperará una imagen en miniatura con las dimensiones de 320 240.

</dd> <dt>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>

<span id="AllocatedGPU"></span><span id="allocatedgpu"></span><span id="ALLOCATEDGPU"></span>**AllocatedGPU** (8)


</dt> <dd>

Esto corresponde a la **propiedad AllocatedGPU** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>

<span id="VirtualSwitchNames"></span><span id="virtualswitchnames"></span><span id="VIRTUALSWITCHNAMES"></span>**VirtualSwitchNames** (9)


</dt> <dd></dd> <dt>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>

<span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Versión** (10)


</dt> <dd>

> [!Note]  
> Se ha agregado Windows 10 y Windows Server 2016.

 

</dd> <dt>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>

<span id="Shielded"></span><span id="shielded"></span><span id="SHIELDED"></span>**Blindada** (11)


</dt> <dd>

> [!Note]  
> Se ha agregado Windows 10, versión 1703 y Windows Server 2016.

 

</dd> <dt>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>

<span id="EnabledState"></span><span id="enabledstate"></span><span id="ENABLEDSTATE"></span>**EnabledState** (100)


</dt> <dd>

Esto corresponde a la **propiedad EnabledState** de la [**clase \_ SummaryInformation de Msvm.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>

<span id="ProcessorLoad"></span><span id="processorload"></span><span id="PROCESSORLOAD"></span>**ProcessorLoad** (101)


</dt> <dd>

Esto corresponde a la **propiedad ProcessorLoad** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>

<span id="ProcessorLoadHistory"></span><span id="processorloadhistory"></span><span id="PROCESSORLOADHISTORY"></span>**ProcessorLoadHistory** (102)


</dt> <dd>

Esto corresponde a la **propiedad ProcessorLoadHistory** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>

<span id="MemoryUsage"></span><span id="memoryusage"></span><span id="MEMORYUSAGE"></span>**MemoryUsage** (103)


</dt> <dd>

Esto corresponde a la **propiedad MemoryUsage** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>

<span id="Heartbeat"></span><span id="heartbeat"></span><span id="HEARTBEAT"></span>**Latido** (104)


</dt> <dd>

Esto corresponde a la propiedad **Heartbeat** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>

<span id="Uptime"></span><span id="uptime"></span><span id="UPTIME"></span>**Tiempo de actividad** (105)


</dt> <dd>

Esto corresponde a la **propiedad UpTime** de la [**clase \_ SummaryInformation de Msvm.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>

<span id="GuestOperatingSystem"></span><span id="guestoperatingsystem"></span><span id="GUESTOPERATINGSYSTEM"></span>**GuestOperatingSystem** (106)


</dt> <dd>

Esto corresponde a la **propiedad GuestOperatingSystem** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>

<span id="Snapshots"></span><span id="snapshots"></span><span id="SNAPSHOTS"></span>**Instantáneas** (107)


</dt> <dd>

Esto corresponde a la **propiedad Snapshots** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>

<span id="AsynchronousTasks"></span><span id="asynchronoustasks"></span><span id="ASYNCHRONOUSTASKS"></span>**AsynchronousTasks** (108)


</dt> <dd>

Esto corresponde a la **propiedad AsynchronousTasks** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>

<span id="HealthState"></span><span id="healthstate"></span><span id="HEALTHSTATE"></span>**HealthState** (109)


</dt> <dd>

Esto corresponde a la **propiedad HealthState** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>

<span id="OperationalStatus"></span><span id="operationalstatus"></span><span id="OPERATIONALSTATUS"></span>**OperationalStatus** (110)


</dt> <dd>

Esto corresponde a la **propiedad OperationalStatus** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>

<span id="StatusDescriptions"></span><span id="statusdescriptions"></span><span id="STATUSDESCRIPTIONS"></span>**StatusDescriptions** (111)


</dt> <dd>

Esto corresponde a la **propiedad StatusDescriptions** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>

<span id="MemoryAvailable"></span><span id="memoryavailable"></span><span id="MEMORYAVAILABLE"></span>**MemoryAvailable** (112)


</dt> <dd>

Esto corresponde a la **propiedad MemoryAvailable** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>

<span id="AvailableMemoryBuffer"></span><span id="availablememorybuffer"></span><span id="AVAILABLEMEMORYBUFFER"></span>**AvailableMemoryBuffer** (113)


</dt> <dd>

Esto corresponde a la **propiedad AvailableMemoryBuffer** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>

<span id="Replication_Mode"></span><span id="replication_mode"></span><span id="REPLICATION_MODE"></span>**Modo de replicación** (114)


</dt> <dd>

Esto corresponde a la **propiedad ReplicationMode** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>

<span id="Replication_State"></span><span id="replication_state"></span><span id="REPLICATION_STATE"></span>**Estado de replicación** (115)


</dt> <dd>

Esto corresponde a la **propiedad ReplicationState** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>

<span id="Replication_HealthTest_Replica_System"></span><span id="replication_healthtest_replica_system"></span><span id="REPLICATION_HEALTHTEST_REPLICA_SYSTEM"></span>**Replication HealthTest Replica System** (116)


</dt> <dd>

Esto corresponde a la **propiedad ReplicationHealth** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>

<span id="Application_Health"></span><span id="application_health"></span><span id="APPLICATION_HEALTH"></span>**Estado de la** aplicación (117)


</dt> <dd></dd> <dt>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>

<span id="ReplicationStateEx"></span><span id="replicationstateex"></span><span id="REPLICATIONSTATEEX"></span>**ReplicationStateEx** (118)


</dt> <dd>

Esto corresponde a la propiedad **ReplicationState** de la [**clase \_ ReplicationRelationship de Msvm.**](msvm-replicationrelationship.md) Se trata de una matriz para todos los valores de estado de replicación en la relación principal y extendida. El valor de índice 0 siempre es para la relación principal y, si la replicación extendida está habilitada, se devuelve en el índice 1.

</dd> <dt>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>

<span id="ReplicationHealthEx"></span><span id="replicationhealthex"></span><span id="REPLICATIONHEALTHEX"></span>**ReplicationHealthEx** (119)


</dt> <dd>

Esto corresponde a la propiedad **ReplicationHealth** de la [**clase \_ ReplicationRelationship de Msvm.**](msvm-replicationrelationship.md) Se trata de una matriz para todos los valores de mantenimiento de replicación en la relación principal y extendida. El valor de índice 0 siempre es para la relación principal y, si la replicación extendida está habilitada, se devuelve en el índice 1.

</dd> <dt>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>

<span id="SwapFilesInUse"></span><span id="swapfilesinuse"></span><span id="SWAPFILESINUSE"></span>**SwapFilesInUse** (120)


</dt> <dd>

Esto corresponde a la **propiedad SwapFilesInUse** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (121)


</dt> <dd></dd> <dt>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>

<span id="ReplicationProviderId"></span><span id="replicationproviderid"></span><span id="REPLICATIONPROVIDERID"></span>**ReplicationProviderId** (122)


</dt> <dd>

Esto corresponde a la **propiedad Name** de la [**clase \_ ReplicationProvider de Msvm.**](msvm-replicationprovider.md)

</dd> <dt>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>

<span id="MemorySpansPhysicalNumaNodes"></span><span id="memoryspansphysicalnumanodes"></span><span id="MEMORYSPANSPHYSICALNUMANODES"></span>**MemorySpansPhysicalNumaNodes** (123)


</dt> <dd></dd> <dt>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>

<span id="IntegrationServicesVersionState"></span><span id="integrationservicesversionstate"></span><span id="INTEGRATIONSERVICESVERSIONSTATE"></span>**IntegrationServicesVersionState** (132)


</dt> <dd>

Esto corresponde a la **propiedad IntegrationServicesVersionState** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>

<span id="OtherEnabledState"></span><span id="otherenabledstate"></span><span id="OTHERENABLEDSTATE"></span>**OtherEnabledState** (132)


</dt> <dd>

Esto corresponde a la **propiedad OtherEnabledState** de la [**clase Msvm \_ SummaryInformation.**](msvm-summaryinformation.md)

</dd> <dt>



 (133)


</dt> <dd></dd> </dl> </dd> <dt>

*SummaryInformation* \[ out\]
</dt> <dd>

Tipo: **[ **Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md)\[\]**

Matriz de [**instancias de Msvm \_ SummaryInformationBase**](msvm-summaryinformationbase.md) que contiene la información solicitada para las máquinas virtuales o instantáneas especificadas en la *matriz SettingData.* Esta matriz tendrá el mismo número de elementos que la *matriz SettingData.* Cada una de estas entradas contendrá la **propiedad Name,** incluso si no se solicitó esta propiedad. Si no se encuentra la máquina virtual o la instantánea o no está disponible, la propiedad **Name** de la entrada de información de resumen correspondiente estará vacía.

Las propiedades no especificadas en *el parámetro RequestedInformation* tendrán un **valor** NULL.

> [!Note]  
> Tipo de datos actualizado desde en Windows 10, versión 1703 de [**Msvm \_ SummaryInformation**](msvm-summaryinformation.md).

 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Parámetros de método comprobados: trabajo iniciado** (4096)
</dt> <dt>

**Error** (32768)
</dt> <dt>

**Acceso denegado** (32769)
</dt> <dt>

**No compatible** (32770)
</dt> <dt>

**El estado es desconocido** (32771)
</dt> <dt>

**Tiempo de** espera (32772)
</dt> <dt>

**Parámetro no** válido (32773)
</dt> <dt>

**El sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

**El sistema no está disponible** (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> </dl>

## <a name="remarks"></a>Observaciones

El acceso a [**la clase Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de C# se muestra información de resumen. Las utilidades a las que se hace referencia se pueden encontrar [en Utilidades comunes para los ejemplos de virtualización (V2).](common-utilities-for-the-virtualization-samples-v2.md)

> [!IMPORTANT]
> Para funcionar correctamente, el código siguiente debe ejecutarse en el servidor host de la máquina virtual y debe ejecutarse con privilegios de administrador.

 


```CSharp
public class GetSummaryInformationClassV2
{
    public static void GetSummaryInformation(string[] vmNames)
    {
        ManagementScope scope = new ManagementScope(@"root\virtualization\v2", null);
        ManagementObject virtualSystemService = Utility.GetServiceObject(scope, "Msvm_VirtualSystemManagementService");
        ManagementBaseObject inParams = virtualSystemService.GetMethodParameters("GetSummaryInformation");

        ManagementObject[] virtualSystemSettings = new ManagementObject[vmNames.Length];

        for (int i = 0; i < vmNames.Length; i++)
        {
            virtualSystemSettings[i] = GetVirtualSystemSetting(vmNames[i], scope);
        }

        UInt32[] requestedInformation = new UInt32[4];
        requestedInformation[0] = 1;    // ElementName
        requestedInformation[2] = 103;  // MemoryUsage
        requestedInformation[3] = 112;  // MemoryAvailable

        inParams["SettingData"] = virtualSystemSettings;
        inParams["RequestedInformation"] = requestedInformation;

        ManagementBaseObject outParams = virtualSystemService.InvokeMethod("GetSummaryInformation", inParams, null);

        if ((UInt32)outParams["ReturnValue"] == ReturnCode.Completed)
        {
            Console.WriteLine("Summary information was retrieved successfully.");

            ManagementBaseObject[] summaryInformationArray = 
                (ManagementBaseObject[])outParams["SummaryInformation"];

            foreach (ManagementBaseObject summaryInformation in summaryInformationArray)
            {
                Console.WriteLine("\nVirtual System Summary Information:");
                if ((null == summaryInformation["Name"]) || 
                    (summaryInformation["Name"].ToString().Length == 0))
                {
                    Console.WriteLine("\tThe VM or snapshot could not be found.");
                }
                else
                {
                    Console.WriteLine("\tName: {0}", summaryInformation["Name"].ToString());
                    foreach (UInt32 requested in requestedInformation)
                    {
                        switch (requested)
                        {
                            case 1:
                                Console.WriteLine("\tElementName: {0}", summaryInformation["ElementName"].ToString());
                                break;

                            case 103:
                                Console.WriteLine("\tMemoryUsage: {0}", summaryInformation["MemoryUsage"].ToString());
                                break;

                            case 112:
                                Console.WriteLine("\tMemoryAvailable: {0}", summaryInformation["MemoryAvailable"].ToString());
                                break;
                        }
                    }
                }
            }
        }
        else
        {
            Console.WriteLine("Failed to retrieve virtual system summary information");
        }

        inParams.Dispose();
        outParams.Dispose();
        virtualSystemService.Dispose();
    }

    public static ManagementObject GetVirtualSystemSetting(string vmName, ManagementScope scope)
    {
        ManagementObject virtualSystem = Utility.GetTargetComputer(vmName, scope);

        ManagementObjectCollection virtualSystemSettings = virtualSystem.GetRelated
         (
             "Msvm_VirtualSystemSettingData",
             "Msvm_SettingsDefineState",
             null,
             null,
             "SettingData",
             "ManagedElement",
             false,
             null
         );

        ManagementObject virtualSystemSetting = null;

        foreach (ManagementObject instance in virtualSystemSettings)
        {
            virtualSystemSetting = instance;
            break;
        }

        return virtualSystemSetting;

    }
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

[**CIM \_ VirtualSystemSettingData**](/previous-versions//cc136954(v=vs.85))
</dt> <dt>

[**Msvm \_ SummaryInformation**](msvm-summaryinformation.md)
</dt> </dl>

 

