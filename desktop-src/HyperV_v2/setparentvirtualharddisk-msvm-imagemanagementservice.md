---
description: Actualiza el elemento primario de los archivos de disco duro virtual de hoja y secundario especificados.
ms.assetid: 5ad41218-bcfd-449a-a66e-2096a1d96bf5
title: Método SetParentVirtualHardDisk de la clase Msvm_ImageManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.SetParentVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f1d14d3b2ee19a9768e1ee9ed9333a452153cc9b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105687462"
---
# <a name="setparentvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Método SetParentVirtualHardDisk de la \_ clase ImageManagementService de MSVM

Actualiza el elemento primario de los archivos de disco duro virtual de hoja y secundario especificados. Vea la sección Comentarios para conocer las restricciones de uso de este método.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SetParentVirtualHardDisk(
  [in]  string              ChildPath,
  [in]  string              ParentPath,
  [in]  string              LeafPath,
  [in]  boolean             IgnoreIDMismatch,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ChildPath* \[ de\]
</dt> <dd>

Ruta de acceso completa que especifica la ubicación del archivo de disco duro virtual secundario.

</dd> <dt>

*ParentPath* \[ de\]
</dt> <dd>

Ruta de acceso completa que especifica la ubicación del archivo de disco duro virtual principal.

</dd> <dt>

*LeafPath* \[ de\]
</dt> <dd>

Ruta de acceso completa que especifica la ubicación del archivo de disco duro virtual de hoja. El parámetro puede ser **null** si el disco duro virtual está sin conexión, pero debe especificarse si el disco duro virtual está en uso.

</dd> <dt>

*IgnoreIDMismatch* \[ de\]
</dt> <dd>

Indica si el elemento primario se debe establecer forzosamente cuando los identificadores de disco virtual no coinciden. Este parámetro debe usarse con precaución porque si el nuevo disco duro virtual principal no es idéntico al primario original, pueden producirse daños en los datos.

</dd> <dt>

*Trabajo* \[ de enuncia\]
</dt> <dd>

Si la operación se realiza de forma asincrónica, este método devolverá 4096 y este parámetro contendrá una referencia a un objeto derivado de [**\_ ConcreteJob CIM**](/previous-versions//cc136808(v=vs.85)).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

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

**Estado desconocido** (32771)
</dt> <dt>

**Tiempo de espera** (32772)
</dt> <dt>

**Parámetro no válido** (32773)
</dt> <dt>

El **sistema está en uso** (32774)
</dt> <dt>

**Estado no válido para esta operación** (32775)
</dt> <dt>

**Tipo de datos incorrecto** (32776)
</dt> <dt>

El **sistema no está disponible** (32777)
</dt> <dt>

**Memoria insuficiente** (32778)
</dt> <dt>

**No se encontró el archivo** (32779)
</dt> </dl>

## <a name="remarks"></a>Observaciones

Solo se pueden usar los siguientes tipos de discos duros virtuales con este método:

-   VHD de diferenciación
-   VHDX de diferenciación

El acceso a la clase [**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md) puede estar restringido por el filtrado de UAC. Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 8 \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2012 \[\]<br/>                                                    |
| Espacio de nombres<br/>                | \\Virtualización de raíz \\ V2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization. v2. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**MSVM \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

