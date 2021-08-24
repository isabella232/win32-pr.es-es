---
description: El método IsPhysicalPresenceHardwareEnabled de la clase Tpm win32 indica si la presencia física en la plataforma se puede establecer \_ con una señal de hardware.
ms.assetid: 65dabfa9-bfbe-4b9b-8e80-02269895c7ad
title: Método IsPhysicalPresenceHardwareEnabled de la Win32_Tpm clase
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalPresenceHardwareEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 499ec39741b23583b599407ef43696ab82164f365626c8042586b6b6e4b56deb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119797045"
---
# <a name="isphysicalpresencehardwareenabled-method-of-the-win32_tpm-class"></a>Método IsPhysicalPresenceHardwareEnabled de la clase Tpm de \_ Win32

El **método IsPhysicalPresenceHardwareEnabled** de la clase [**\_ Tpm win32**](win32-tpm.md) indica si la presencia física en la plataforma se puede establecer con una señal de hardware. El fabricante de la plataforma configura este valor en función del diseño de la plataforma. La documentación del fabricante de la plataforma puede proporcionar información adicional.

## <a name="syntax"></a>Sintaxis


```mof
uint32 IsPhysicalPresenceHardwareEnabled(
  [out] boolean IsPhysicalPresenceHardwareEnabled
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*IsPhysicalPresenceHardwareEnabled* \[ out\]
</dt> <dd>

Tipo: **booleano**

Si **es true,** la presencia física en la plataforma se puede establecer con una señal de hardware.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **uint32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

A continuación se enumeran los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>**S \_ Ok**</dt> <dt>0 (0x0)</dt> </dl> | Método realizado correctamente.<br/> |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del SDK Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](../wmisdk/managed-object-format--mof-.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                            |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                      |
| Espacio de nombres<br/>                | Root \\ CIMV2 \\ Security \\ MicrosoftTpm<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ tpm.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Win32 \_tpm.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Tpm de \_ Win32**](win32-tpm.md)
</dt> </dl>

 

 
