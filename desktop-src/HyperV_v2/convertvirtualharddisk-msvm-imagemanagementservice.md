---
description: Convierte un disco duro virtual existente a un tipo o formato diferente.
ms.assetid: D4F3A030-D860-4569-B6CD-31661BD40D54
title: Método ConvertVirtualHardDisk de la Msvm_ImageManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.ConvertVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 1da8a842f00af68d5fb07a23ec9d12a99d48b0669e00c1e1f2997bf7ef941767
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119532585"
---
# <a name="convertvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Método ConvertVirtualHardDisk de la clase \_ Msvm ImageManagementService

Convierte un disco duro virtual existente a un tipo o formato diferente. Este método crea un nuevo disco duro virtual y no convierte el disco duro virtual de origen en su lugar. Vea Comentarios sobre las restricciones de uso para este método.

## <a name="syntax"></a>Sintaxis


```mof
uint32 ConvertVirtualHardDisk(
  [in]  string              SourcePath,
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SourcePath* \[ En\]
</dt> <dd>

Tipo: **cadena**

Ruta de acceso completa del archivo de disco duro virtual de origen que se convertirá. Este archivo no se modificará como resultado de esta operación.

</dd> <dt>

*VirtualDiskSettingData* \[ En\]
</dt> <dd>

Tipo: **cadena**

Representación de cadena de la [**clase \_ VirtualHardDiskSettingData de Msvm**](msvm-virtualharddisksettingdata.md) que especifica los atributos del nuevo disco duro virtual. Se **deben** establecer las propiedades Path , **Type**, **Format**, **ParentPath**, **BlockSize** y **LogicalSectorSize.** La **propiedad ParentPath** puede ser **Null** si no es necesaria. Establezca las **propiedades BlockSize** **y LogicalSectorSize** en 0 para usar los valores predeterminados.

Para especificar el formato (VHD o VHDX) del nuevo disco duro virtual, establezca la extensión de **la** ruta de acceso en el valor adecuado (".vhd" o ".vhdx"). La **propiedad Format** debe coincidir con la extensión de nombre de archivo en la ruta de **acceso**.

Se omitirá la propiedad **LogicalSectorSize.**

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Tipo: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método puede devolver uno de los valores siguientes.

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

**El sistema no está** disponible (32777)
</dt> <dt>

**Memoria sin memoria** (32778)
</dt> <dt>

**Archivo no encontrado** (32779)
</dt> </dl>

## <a name="remarks"></a>Comentarios

Con este método solo se pueden usar los siguientes tipos de discos duros virtuales:

-   Disco duro virtual fijo
-   VHDX corregido
-   VHD dinámico
-   VHDX dinámico
-   Disco duro virtual de diferenciación
-   Diferenciación de VHDX

El acceso a [**la clase \_ ImageManagementService de Msvm**](msvm-imagemanagementservice.md) podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de C# se convierte un disco duro virtual. Las utilidades a las que se hace referencia se pueden encontrar [en Utilidades comunes para los ejemplos de virtualización (V2).](common-utilities-for-the-virtualization-samples-v2.md)


```CSharp
public enum VirtualHardDiskType
{
    Fixed = 2,
    Dynamic = 3,
    Differencing = 4
}

public enum VirtualHardDiskFormat
{
    Unknown = 0,
    Vhd = 2,
    Vhdx = 3
}

public static void ConvertVirtualHardDisk(string sourcePath, string destinationPath, VirtualHardDiskType diskType, VirtualHardDiskFormat diskFormat)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementPath path = new ManagementPath()
    {
        Server = null,
        NamespacePath = imageService.Path.Path,
        ClassName = "Msvm_VirtualHardDiskSettingData"
    };

    ManagementClass settingsClass = new ManagementClass(path);
    ManagementObject settingsInstance = settingsClass.CreateInstance();
    settingsInstance["Path"] = destinationPath;
    settingsInstance["Type"] = diskType;
    settingsInstance["Format"] = diskFormat;
    settingsInstance["ParentPath"] = null;
    settingsInstance["MaxInternalSize"] = 0;
    settingsInstance["BlockSize"] = 0;
    settingsInstance["LogicalSectorSize"] = 0;
    settingsInstance["PhysicalSectorSize"] = 0;

    ManagementBaseObject inParams = imageService.GetMethodParameters("ConvertVirtualHardDisk");

    inParams["SourcePath"] = sourcePath;
    inParams["VirtualDiskSettingData"] = settingsInstance.GetText(TextFormat.WmiDtd20);

    ManagementBaseObject outParams = imageService.InvokeMethod("ConvertVirtualHardDisk", inParams, null);
    UInt32 result = (UInt32)outParams["ReturnValue"];
    if (ReturnCode.Completed == result)
    {
        Console.WriteLine("{0} was converted successfully.", inParams["SourcePath"]);
    }
    else if (ReturnCode.Started == result)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was converted successfully.", inParams["SourcePath"]);
        }
        else
        {
            Console.WriteLine("Unable to convert {0}", inParams["SourcePath"]);
        }
    }
    else
    {
        // The method failed.
        Console.WriteLine("ConvertVirtualHardDisk failed with error code {0}.", result);
    }

    outParams.Dispose();
    inParams.Dispose();
    imageService.Dispose();
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8 solo aplicaciones de escritorio\]<br/>                                                              |
| Servidor mínimo compatible<br/> | \[Windows Server 2012 solo aplicaciones de escritorio\]<br/>                                                    |
| Espacio de nombres<br/>                | Root \\ Virtualization \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization.V2.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ConvertVirtualHardDisk (V1)**](/previous-versions/windows/desktop/virtual/convertvirtualharddisk-msvm-imagemanagementservice)
</dt> <dt>

[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))
</dt> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

