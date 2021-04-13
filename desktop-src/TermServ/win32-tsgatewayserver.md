---
title: Win32_TSGatewayServer (clase)
description: Se usa para las operaciones específicas del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).
ms.assetid: ae24b7ff-2c26-43a5-ac11-52f83225f4ee
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServer clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSGatewayServer de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSGatewayServer
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b7dee009521c59b606010be085fcb0447558898d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490276"
---
# <a name="win32_tsgatewayserver-class"></a>\_Clase Win32 TSGatewayServer

Se usa para las operaciones específicas del servidor de puerta de enlace de Escritorio remoto (puerta de enlace de escritorio remoto).

## <a name="syntax"></a>Sintaxis

``` syntax
[singleton, dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayServer
{
};
```

## <a name="members"></a>Miembros

La **clase \_ TSGatewayServer de Win32** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La clase **Win32 \_ TSGatewayServer** tiene estos métodos.



| Método                                                                                   | Descripción                                                                                                                    |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**CreateSelfSignedCertificate**](createselfsignedcertificate-win32-tsgatewayserver.md) | Crea un certificado autofirmado con un nombre de sujeto determinado y devuelve el hash del certificado como un parámetro "out".<br/> |
| [**Exportación**](export-win32-tsgatewayserver.md)                                           | Devuelve la configuración del servidor de puerta de enlace de escritorio remoto como una cadena XML.<br/>                                                       |
| [**Importar**](import-win32-tsgatewayserver.md)                                           | Importa una configuración determinada en el servidor de puerta de enlace de escritorio remoto.<br/>                                                             |



 

## <a name="remarks"></a>Observaciones

Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI). Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | Raíz de \\ CIMv2 \\ TerminalServices<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway. mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



 

