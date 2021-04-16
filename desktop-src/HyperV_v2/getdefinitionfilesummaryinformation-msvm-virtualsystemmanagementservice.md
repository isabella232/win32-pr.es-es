---
description: Devuelve información de Resumen de la máquina virtual para los archivos de definición de máquina virtual especificados.
ms.assetid: 5a3d7f2c-3b89-4dd6-909d-4452afc3705f
title: Método GetDefinitionFileSummaryInformation de la clase Msvm_VirtualSystemManagementService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetDefinitionFileSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a46daedd282d07c2367931a9f20a7fbfa1849f9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686892"
---
# <a name="getdefinitionfilesummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Método GetDefinitionFileSummaryInformation de la \_ clase VirtualSystemManagementService de MSVM

Devuelve información de Resumen de la máquina virtual para los archivos de definición de máquina virtual especificados.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetDefinitionFileSummaryInformation(
  [in]  string                      DefinitionFiles[],
  [out] Msvm_SummaryInformationBase SummaryInformation[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*DefinitionFiles* \[ de\]
</dt> <dd>

Matriz de rutas de acceso a los archivos de configuración XML para los que se va a devolver información de resumen.

</dd> <dt>

*SummaryInformation* \[ enuncia\]
</dt> <dd>

Una matriz de instancias de [**MSVM \_ SummaryInformationBase**](msvm-summaryinformation.md) que contiene la información solicitada para las máquinas virtuales y/o las instantáneas especificadas en la matriz *DefinitionFiles* . Solo se devuelven las propiedades **Name**, **ElementName**, **CreationTime** y **Notes** , todas las demás propiedades serán **null**.

> [!Note]  

 

Antes de Windows 10, versión 1703, DataType era [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md).

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
</dt> </dl>

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

[**MSVM \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




