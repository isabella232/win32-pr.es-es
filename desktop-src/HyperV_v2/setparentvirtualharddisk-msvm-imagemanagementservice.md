---
description: Actualiza el elemento primario de los archivos de disco duro virtual hoja y secundario especificados.
ms.assetid: 5ad41218-bcfd-449a-a66e-2096a1d96bf5
title: Método SetParentVirtualHardDisk de la Msvm_ImageManagementService clase
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
ms.openlocfilehash: 47be9f3f383da237a3679633ac1d663bbc81ef078a7529662b8f21d10246761f
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050545"
---
# <a name="setparentvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a>Método SetParentVirtualHardDisk de la clase \_ Msvm ImageManagementService

Actualiza el elemento primario de los archivos de disco duro virtual hoja y secundario especificados. Vea Comentarios sobre las restricciones de uso para este método.

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

*ChildPath* \[ En\]
</dt> <dd>

Ruta de acceso completa que especifica la ubicación del archivo de disco duro virtual secundario.

</dd> <dt>

*ParentPath* \[ En\]
</dt> <dd>

Ruta de acceso completa que especifica la ubicación del archivo de disco duro virtual primario.

</dd> <dt>

*LeafPath* \[ En\]
</dt> <dd>

Ruta de acceso completa que especifica la ubicación del archivo de disco duro virtual hoja. El parámetro puede ser **Null si** el disco duro virtual está sin conexión, pero debe especificarse si el disco duro virtual está en uso.

</dd> <dt>

*IgnoreIDMismatch* \[ En\]
</dt> <dd>

Indica si el elemento primario debe establecerse forzadamente cuando los identificadores de disco virtual no coinciden. Este parámetro debe usarse con precaución porque si el nuevo disco duro virtual primario no es idéntico al primario original, pueden producirse daños en los datos.

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

-   Disco duro virtual de diferenciación
-   Diferenciación de VHDX

El acceso a [**la clase \_ ImageManagementService de Msvm**](msvm-imagemanagementservice.md) podría estar restringido por el filtrado de UAC. Para obtener más información, vea [Control de cuentas de usuario y WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)

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

[**Msvm \_ ImageManagementService**](msvm-imagemanagementservice.md)
</dt> </dl>

 

