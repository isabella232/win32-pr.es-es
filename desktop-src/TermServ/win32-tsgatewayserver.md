---
title: Win32_TSGatewayServer clase
description: Se usa para Escritorio remoto gateway (puerta de enlace de Escritorio remoto) específicas del servidor.
ms.assetid: ae24b7ff-2c26-43a5-ac11-52f83225f4ee
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayServer clase Servicios de Escritorio remoto
- Win32_TSGatewayServer clase Servicios de Escritorio remoto , descrita
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
ms.openlocfilehash: 43cd6c24447e7ba3bc22788484b2ac9e437ee947243c17a676728d2a336bd326
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118603896"
---
# <a name="win32_tsgatewayserver-class"></a>Clase \_ TSGatewayServer de Win32

Se usa para Escritorio remoto gateway (puerta de enlace de Escritorio remoto) específicas del servidor.

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

La **clase \_ TSGatewayServer de Win32** tiene estos métodos.



| Método                                                                                   | Descripción                                                                                                                    |
|:-----------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**CreateSelfSignedCertificate**](createselfsignedcertificate-win32-tsgatewayserver.md) | Crea un certificado autofirmado con un nombre de sujeto determinado y devuelve el hash del certificado como un parámetro "out".<br/> |
| [**exportar**](export-win32-tsgatewayserver.md)                                           | Devuelve la configuración del servidor de puerta de enlace de Escritorio remoto como una cadena XML.<br/>                                                       |
| [**Importar**](import-win32-tsgatewayserver.md)                                           | Importa una configuración determinada al servidor de puerta de enlace de Escritorio remoto.<br/>                                                             |



 

## <a name="remarks"></a>Comentarios

Managed Object Format (MOF) contienen las definiciones de las Windows instrumental de administración de recursos (WMI). Los archivos MOF no se instalan como parte del Kit de desarrollo de software (SDK) de Microsoft Windows. Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor. Para obtener más información sobre los archivos MOF, [vea Managed Object Format (MOF).](/windows/desktop/WmiSdk/managed-object-format--mof-)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | No se admite ninguno<br/>                                                                |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                           |
| Espacio de nombres<br/>                | \\TerminalServices de CIMv2 \\ raíz<br/>                                                 |
| MOF<br/>                      | <dl> <dt>TSGateway.mof</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>AagWmi.dll</dt> </dl>    |



 

