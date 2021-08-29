---
description: Desasoje la imagen de almacenamiento montada asociada a esta clase.
ms.assetid: C3AB0EEE-71FE-4049-90AB-01F5D77E3B97
title: Método DetachVirtualHardDisk de la Msvm_MountedStorageImage clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MountedStorageImage.DetachVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 8ee19316b5e3cbf5440a243df283379b863ecd026b53471b04dfa01ca6731825
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119682565"
---
# <a name="detachvirtualharddisk-method-of-the-msvm_mountedstorageimage-class"></a>Método DetachVirtualHardDisk de la clase \_ Msvm MountedStorageImage

Desasoje la imagen de almacenamiento montada asociada a esta clase.

## <a name="syntax"></a>Sintaxis


```mof
uint32 DetachVirtualHardDisk();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Este método puede devolver uno de los valores siguientes.

<dl> <dt>

**Correcto** (0)
</dt> <dt>

**Error** (1)
</dt> </dl>

## <a name="remarks"></a>Comentarios

El acceso a [**la clase \_ Msvm MountedStorageImage**](msvm-mountedstorageimage.md) podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo de C# se muestra cómo separar un archivo de disco duro virtual. Las utilidades a las que se hace referencia se pueden encontrar [en Utilidades comunes para los ejemplos de virtualización (V2).](common-utilities-for-the-virtualization-samples-v2.md)


```CSharp
public static void DetachVirtualHardDisk(string path)
{
    ManagementScope scope = new ManagementScope(@"root\virtualization\V2", null);

    ManagementClass mountedStorageImageServiceClass = new ManagementClass("Msvm_MountedStorageImage");

    mountedStorageImageServiceClass.Scope = scope;

    using (ManagementObjectCollection collection = mountedStorageImageServiceClass.GetInstances())
    {
        foreach (ManagementObject image in collection)
        {
            using (image)
            {
                string name = image.GetPropertyValue("Name").ToString();
                if (string.Equals(name, path, StringComparison.OrdinalIgnoreCase))
                {
                    ManagementBaseObject outParams = image.InvokeMethod("DetachVirtualHardDisk", null, null);

                    if ((UInt32)outParams["ReturnValue"] == 0)
                    {
                        Console.WriteLine("{0} was detached successfully.", path);
                    }
                    else
                    {
                        Console.WriteLine("Unable to dettach {0}", path);
                    }

                    outParams.Dispose();

                    break;
                }

                image.Dispose();
            }
        }
    }
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

[**Msvm \_ MountedStorageImage**](msvm-mountedstorageimage.md)
</dt> </dl>

 

