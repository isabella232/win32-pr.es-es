---
title: Método GetProvisioningProperties de la Win32_RDMSCollectionProperties clase
description: Recupera las propiedades de aprovisionamiento de la colección de escritorios virtuales.
ms.assetid: c314b7a5-8546-4711-833e-b47bb682aa53
ms.tgt_platform: multiple
keywords:
- Método GetProvisioningProperties Servicios de Escritorio remoto
- Método GetProvisioningProperties Servicios de Escritorio remoto , Win32_RDMSCollectionProperties clase
- Win32_RDMSCollectionProperties clase Servicios de Escritorio remoto método , GetProvisioningProperties
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
ms.openlocfilehash: 4cd97ca6f3ec79320509881d79bc0ea24d73944a0ae3634d331073517c8bc0fe
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118130450"
---
# <a name="getprovisioningproperties-method-of-the-win32_rdmscollectionproperties-class"></a>Método GetProvisioningProperties de la clase RDMSCollectionProperties de Win32 \_

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

*PoolVhdType* \[ out\]
</dt> <dd>

Especifica el formato vhd (disco duro virtual) del grupo de máquinas virtuales de la colección.

<dt>

Clonar
</dt> <dd>

Vhd clonado.

</dd> <dt>

DiffDisk
</dt> <dd>

Vhd de diferenciación.

</dd> </dl> </dd> <dt>

*MasterVmLocation* \[ out\]
</dt> <dd>

Recibe la ruta de acceso a la imagen de máquina virtual maestra.

</dd> <dt>

*NamePrefix* \[ out\]
</dt> <dd>

Recibe el prefijo de nombre que se anexará al principio de los nombres de máquina virtual.

</dd> <dt>

*NameStartIndex* \[ out\]
</dt> <dd>

Índice inicial.

</dd> <dt>

*LocalVmLocation* \[ out\]
</dt> <dd>

Recibe la ruta de acceso local a las máquinas virtuales en los servidores de Hyper-V. Si este parámetro se establece en **NULL** o si está vacío, se usará el directorio de máquina virtual predeterminado.

</dd> <dt>

*LocalGoldVmLocation* \[ out\]
</dt> <dd>

Recibe la ruta de acceso local a la imagen de VHD golden cuando el *parámetro PoolVhdTpe* está establecido en "DiffDisk". Si este parámetro se establece en **NULL** o si está vacío, se usará el directorio de máquina virtual predeterminado.

</dd> <dt>

*RunFromSMB* \[ out\]
</dt> <dd>

Recibe un valor que indica si se debe ejecutar la colección desde un recurso compartido bloque de mensajes del servidor (SMB). **TRUE** para ejecutar las máquinas virtuales desde un recurso compartido SBM; de lo contrario; **FALSE**.

</dd> <dt>

*SMBLocation* \[ out\]
</dt> <dd>

Recibe la ruta de acceso al recurso compartido SMB si está habilitado el uso compartido de SMB.

</dd> <dt>

*SMBStreaming* \[ out\]
</dt> <dd>

Recibe un valor que indica si está habilitada la transmisión por secuencias SMB. **TRUE si** el uso compartido de SMB está habilitado; de lo contrario; **FALSE**.

</dd> <dt>

*VmDomain* \[ out\]
</dt> <dd>

Recibe el nombre de dominio de las máquinas virtuales de la colección.

</dd> <dt>

*VmOU* \[ out\]
</dt> <dd>

Recibe el Active Directory unidad organizativa (OU) de las máquinas virtuales de la colección.

</dd> <dt>

*ProductKey* \[ out\]
</dt> <dd>

Recibe las claves de producto del sistema operativo para las máquinas virtuales de la colección.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve 0 si se ejecuta correctamente; de lo contrario, devuelve un código de error WMI.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                              |
| Espacio de nombres<br/>                | Rdms \\ de CIMv2 \\ raíz<br/>                                                                |
| MOF<br/>                      | <dl> <dt>RDManagement.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**RdMSCollectionProperties de Win32 \_**](win32-rdmscollectionproperties.md)
</dt> </dl>

 

 





