---
description: Realiza una prueba automática del TPM y devuelve el resultado.
ms.assetid: 0f8fdb68-80b1-4fc4-beb9-e87f51b85031
title: Método SelfTest de la clase Win32_Tpm
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.SelfTest
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 8681ee8ca49b8b2f7de550ffc5baa0ff8c0c9470
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666382"
---
# <a name="selftest-method-of-the-win32_tpm-class"></a>Método SelfTest de la \_ clase Win32 TPM

El método **SelfTest** de la clase [**Win32 \_ TPM**](win32-tpm.md) realiza una prueba automática del TPM y devuelve el resultado.

Una prueba automática de TPM se ejecuta automáticamente cuando se inicia el equipo.

## <a name="syntax"></a>Sintaxis


```mof
uint32 SelfTest(
  [out] uint8 SelfTestResult[]
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*SelfTestResult* \[ enuncia\]
</dt> <dd>

Tipo: **Uint8 \[ \]**

Matriz de bytes que contiene el resultado de la prueba automática. El formato de este parámetro es específico del fabricante.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **UInt32**

Se pueden devolver todos los errores de TPM, así como los errores específicos de los servicios base de TPM.

En la tabla siguiente se enumeran algunos de los códigos de retorno comunes.



| Código o valor devuelto                                                                                                                                 | Descripción                             |
|---------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> <dt>0 (0X0)</dt> </dl> | El método se ejecutó correctamente.<br/> |



 

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte de la Windows SDK. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                            |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                      |
| Espacio de nombres<br/>                | \\MicrosoftTpm de \\ seguridad de cimv2 raíz \\<br/>                                            |
| MOF<br/>                      | <dl> <dt>Win32 \_ TPM. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>\_tpm.dllWin32</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**TPM de Win32 \_**](win32-tpm.md)
</dt> </dl>

 

 
