---
title: Propiedad nombre de IVMVirtualMachine (VPCCOMInterfaces. h)
description: Nombre de la configuración de la máquina virtual.
ms.assetid: 90acedbf-4159-48a3-a9e9-6f1ee00dab8b
keywords:
- Propiedad nombre virtual PC
- Propiedad nombre virtual PC, interfaz IVMVirtualMachine
- Interfaz IVMVirtualMachine Virtual PC, propiedad Name
topic_type:
- apiref
api_name:
- IVMVirtualMachine.Name
- IVMVirtualMachine.get_Name
- IVMVirtualMachine.put_Name
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c163173a778d8103922fd8c8948ab5156f512ed0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150426"
---
# <a name="ivmvirtualmachinename-property"></a>IVMVirtualMachine:: Name (propiedad)

\[Windows Virtual PC ya no está disponible para su uso a partir de Windows 8. En su lugar, use el [proveedor de WMI de Hyper-V (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Recupera y establece el nombre de la configuración de la máquina virtual.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_Name(
  [in]          BSTR virtualMachineName
);

HRESULT get_Name(
  [out, retval] BSTR *virtualMachineName
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica el nombre de la configuración de la máquina virtual. La longitud del nombre no puede superar los 80 caracteres y la longitud total de la ruta de acceso completa que incluye el archivo de configuración del nombre de la máquina virtual no puede superar los caracteres de la **\_ ruta de acceso máxima** (260).

## <a name="error-codes"></a>Códigos de error



| Nombre o valor                                                                                                                                                                    | Significado                                                                                         |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <dl> <dt>S \_ Aceptar</dt> <dt>0</dt> </dl>                                       | La operación se realizó correctamente.<br/>                                                        |
| <dl> <dt>E \_ PUNTERO</dt> <dt>0x80004003</dt> </dl>                         | El parámetro es **null**.<br/>                                                           |
| <dl> <dt>E \_ INVALIDARG</dt> <dt>0x80000003</dt> </dl>                      | El parámetro no es válido o es una cadena vacía.<br/>                                    |
| <dl> <dt>Máquina virtual \_ 0xA0040207 de \_ máquina virtual \_ desconocida</dt> <dt></dt> </dl>                 | La configuración es desconocida.<br/>                                                        |
| <dl> <dt>Máquina virtual \_ E \_ preft \_ VM \_ Active</dt> <dt>0xA0040302</dt> </dl>            | La máquina virtual está en ejecución o guardada.<br/>                                             |
| <dl> <dt>Máquina virtual \_ E \_ configuración \_ sin \_ nombre</dt> <dt>0xA0040400</dt> </dl>            | El parámetro *virtualMachineName* está vacío.<br/>                                         |
| <dl> <dt>Máquina virtual \_ E \_ nombre de configuración \_ \_ demasiado \_ largo</dt> <dt>0xA00400401</dt> </dl>    | El parámetro contiene demasiados caracteres.<br/>                                          |
| <dl> <dt>Máquina virtual \_ E \_ nombre de configuración de 0xA0040402 \_ \_ \_ Char no válido</dt> <dt></dt> </dl> | El parámetro contiene uno de los siguientes caracteres no válidos " \* ?: <>/ \| \\ " ".<br/> |
| <dl> <dt>Máquina virtual \_ E \_ configuración \_ \_ nombre duplicado</dt> <dt>0xA0040403</dt> </dl>     | El nombre especificado ya existe como el nombre de otra máquina virtual.<br/>            |
| <dl> <dt>DISP \_ . E \_ excepción</dt> <dt>0x80020009</dt> </dl>                 | Se produjo un error inesperado.<br/>                                                    |



## <a name="remarks"></a>Observaciones

Los nombres de las máquinas virtuales no distinguen mayúsculas de minúsculas, por ejemplo, "MyVM" y "MyVM" hacen referencia a la misma máquina virtual. Esta es la propiedad predeterminada para [**IVMVirtualMachine**](ivmvirtualmachine.md).

Si VPC.exe se está ejecutando y la máquina virtual se guarda, el establecimiento de la propiedad **Name** no se realizará correctamente. Si VPC.exe no se está ejecutando y se guarda la máquina virtual, el establecimiento de la propiedad **Name** se realizará correctamente cuando se inicie VPC.exe.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                    |
| Servidor mínimo compatible<br/> | No se admite ninguno<br/>                                                                     |
| Fin de compatibilidad de cliente<br/>    | Windows 7<br/>                                                                          |
| Producto<br/>                  | Windows Virtual PC<br/>                                                                 |
| Encabezado<br/>                   | <dl> <dt>VPCCOMInterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ IVMVirtualMachine se define como f7092aa1-33ed-4f78-a59f-c00adfc2edd7<br/>          |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IVMVirtualMachine**](ivmvirtualmachine.md)
</dt> </dl>

 

