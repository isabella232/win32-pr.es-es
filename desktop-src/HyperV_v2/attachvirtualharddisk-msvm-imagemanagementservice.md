---
description: Adjunta un archivo de disco duro virtual en modo de bucle recuperación.
ms.assetid: 54bd8e67-e309-4bf3-94bd-e29bc3300a3d
title: Método AttachVirtualHardDisk de la Msvm_ImageManagementService clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.AttachVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: ab8ec59dfb148a0ed72cf469e43befb7857caae5e7045553d9fda2c586fcd563
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117813652"
---
# <a name="attachvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Método AttachVirtualHardDisk de la clase \_ Msvm ImageManagementService

Adjunta un archivo de disco duro virtual en modo de bucle recuperación.

## <a name="syntax"></a>Sintaxis


```mof
uint32 AttachVirtualHardDisk(
  [in]  string              Path,
  [in]  boolean             AssignDriveLetter,
  [in]  boolean             ReadOnly,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Ruta de acceso* \[ En\]
</dt> <dd>

Ruta de acceso completa que especifica la ubicación del archivo de disco duro virtual que se adjuntará.

</dd> <dt>

*AssignDriveLetter* \[ En\]
</dt> <dd>

Indica si se asignan letras de unidad a los volúmenes del disco.

</dd> <dt>

*ReadOnly* \[ En\]
</dt> <dd>

Indica si el disco duro conectado debe ser de solo lectura.

</dd> <dt>

*Trabajo* \[ out\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método devuelve uno de los valores siguientes.

<dl> <dt>

**Completado sin error** (0)
</dt> <dt>

**Parámetros de método activados: trabajo iniciado** (4096)
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

Para separar el disco duro virtual, use el método [**\_ Msvm MountedStorageImage.DetachVirtualHardDisk.**](detachvirtualharddisk-msvm-mountedstorageimage.md)

El acceso a [**la clase \_ ImageManagementService de Msvm**](msvm-imagemanagementservice.md) podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de C# se muestra cómo conectar un archivo de disco duro virtual. Las utilidades a las que se hace referencia se pueden encontrar [en Utilidades comunes para los ejemplos de virtualización (V2).](common-utilities-for-the-virtualization-samples-v2.md)


```CSharp
public static void AttachVirtualHardDisk(string path)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);
    ManagementObject imageService = Utility.GetServiceObject(scope, "Msvm_ImageManagementService");

    ManagementBaseObject inParams = imageService.GetMethodParameters("AttachVirtualHardDisk");
    inParams["Path"] = path;
    inParams["AssignDriveLetter"] = true;
    inParams["ReadOnly"] = false;
    ManagementBaseObject outParams = imageService.InvokeMethod("AttachVirtualHardDisk", inParams, null);
    if ((UInt32)outParams["ReturnValue"] == ReturnCode.Started)
    {
        if (Utility.JobCompleted(outParams, scope))
        {
            Console.WriteLine("{0} was attached successfully.", inParams["Path"]);
        }
        else
        {
            Console.WriteLine("Unable to attach {0}", inParams["Path"]);
        }
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

[**Msvm \_ MountedStorageImage.DetachVirtualHardDisk**](detachvirtualharddisk-msvm-mountedstorageimage.md)
</dt> <dt>

[**Montaje (V1)**](/previous-versions/windows/desktop/virtual/mount-msvm-imagemanagementservice)
</dt> <dt>

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

