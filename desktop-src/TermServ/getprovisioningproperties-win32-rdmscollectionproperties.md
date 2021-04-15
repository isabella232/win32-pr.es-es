---
title: Método GetProvisioningProperties de la clase Win32_RDMSCollectionProperties
description: Recupera las propiedades de aprovisionamiento de la colección de escritorios virtuales.
ms.assetid: c314b7a5-8546-4711-833e-b47bb682aa53
ms.tgt_platform: multiple
keywords:
- Método GetProvisioningProperties Servicios de Escritorio remoto
- Método GetProvisioningProperties Servicios de Escritorio remoto, clase Win32_RDMSCollectionProperties
- Win32_RDMSCollectionProperties de clase Servicios de Escritorio remoto, método GetProvisioningProperties
topic_type:
- apiref
api_name:
- Win32_RDMSCollectionProperties.GetProvisioningProperties
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ca58f82d2918441e5da3cf53d442497c1a6a2eb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105686072"
---
# <a name="getprovisioningproperties-method-of-the-win32_rdmscollectionproperties-class"></a>Método GetProvisioningProperties de la \_ clase RDMSCollectionProperties de Win32

Recupera las propiedades de aprovisionamiento de la colección de escritorios virtuales.

## <a name="syntax"></a>Sintaxis


```mof
uint32 GetProvisioningProperties(
  [out] string  PoolVhdType,
  [out] string  MasterVmLocation,
  [out] string  NamePrefix,
  [out] uint32  NameStartIndex,
  [out] string  LocalVmLocation,
  [out] string  LocalGoldVmLocation,
  [out] boolean RunFromSMB,
  [out] string  SMBLocation,
  [out] boolean SMBStreaming,
  [out] string  VmDomain,
  [out] string  VmOU,
  [out] string  ProductKey
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*PoolVhdType* \[ enuncia\]
</dt> <dd>

Especifica el formato VHD (disco duro virtual) del grupo de máquinas virtuales de la colección.

<dt>

Clonar
</dt> <dd>

Un VHD clonado.

</dd> <dt>

DiffDisk
</dt> <dd>

Un VHD de diferenciación.

</dd> </dl> </dd> <dt>

*MasterVmLocation* \[ enuncia\]
</dt> <dd>

Recibe la ruta de acceso a la imagen de máquina virtual maestra.

</dd> <dt>

*NamePrefix* \[ enuncia\]
</dt> <dd>

Recibe el prefijo de nombre que se va a anexar al principio de los nombres de las máquinas virtuales.

</dd> <dt>

*NameStartIndex* \[ enuncia\]
</dt> <dd>

Índice de inicio.

</dd> <dt>

*LocalVmLocation* \[ enuncia\]
</dt> <dd>

Recibe la ruta de acceso local a las máquinas virtuales en los servidores de Hyper-V. Si este parámetro se establece en **null** o está vacío, se usará el directorio predeterminado de la máquina virtual.

</dd> <dt>

*LocalGoldVmLocation* \[ enuncia\]
</dt> <dd>

Recibe la ruta de acceso local a la imagen del VHD Golden cuando el parámetro *PoolVhdTpe* se establece en "DiffDisk". Si este parámetro se establece en **null** o está vacío, se usará el directorio predeterminado de la máquina virtual.

</dd> <dt>

*RunFromSMB* \[ enuncia\]
</dt> <dd>

Recibe un valor que indica si se va a ejecutar la colección desde un recurso compartido de bloque de mensajes del servidor (SMB). **True** para ejecutar las máquinas virtuales desde un recurso compartido SBM; casos **False**.

</dd> <dt>

*SMBLocation* \[ enuncia\]
</dt> <dd>

Recibe la ruta de acceso al recurso compartido de SMB si está habilitado el uso compartido de SMB.

</dd> <dt>

*SMBStreaming* \[ enuncia\]
</dt> <dd>

Recibe un valor que indica si está habilitada la transmisión por secuencias de SMB. **True** si está habilitado el uso compartido de SMB; casos **False**.

</dd> <dt>

*VmDomain* \[ enuncia\]
</dt> <dd>

Recibe el nombre de dominio de las máquinas virtuales de la colección.

</dd> <dt>

*VmOU* \[ enuncia\]
</dt> <dd>

Recibe el Active Directory unidad organizativa (OU) de las máquinas virtuales de la colección.

</dd> <dt>

*ProductKey* \[ enuncia\]
</dt> <dd>

Recibe las claves de producto del sistema operativo para las máquinas virtuales de la colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error de WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | RDMs raíz de \\ CIMv2 \\<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Win32 \_ RDMSCollectionProperties**](win32-rdmscollectionproperties.md)
</dt> </dl>

 

 





