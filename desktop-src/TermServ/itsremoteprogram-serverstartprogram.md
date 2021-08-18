---
title: Método ITSRemoteProgram ServerStartProgram
description: Especifica un programa RemoteApp que se iniciará en la sesión remota.
ms.assetid: 5fb251bf-4832-4e35-b372-23418c280350
ms.tgt_platform: multiple
keywords:
- Método ServerStartProgram Servicios de Escritorio remoto
- Método ServerStartProgram Servicios de Escritorio remoto , interfaz ITSRemoteProgram
- Interfaz ITSRemoteProgram Servicios de Escritorio remoto , método ServerStartProgram
- Método ServerStartProgram Servicios de Escritorio remoto , interfaz ITSRemoteProgram2
- Interfaz ITSRemoteProgram2 Servicios de Escritorio remoto , método ServerStartProgram
- Método ServerStartProgram Servicios de Escritorio remoto , interfaz ITSRemoteProgram3
- Interfaz ITSRemoteProgram3 Servicios de Escritorio remoto , método ServerStartProgram
topic_type:
- apiref
api_name:
- ITSRemoteProgram.ServerStartProgram
- ITSRemoteProgram2.ServerStartProgram
- ITSRemoteProgram3.ServerStartProgram
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c789a9963086128e93546415247cfb3db69afe59c67a445b851ee5cf3687d16c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117756861"
---
# <a name="itsremoteprogramserverstartprogram-method"></a>Método ITSRemoteProgram::ServerStartProgram

Especifica un programa RemoteApp que se iniciará en la sesión remota. Esta función debe invocarse en una sesión conectada (después de recibir la notificación conectada a la sesión en el cliente). Cualquier número de programas RemoteApp se puede iniciar en una sesión. Una sesión de RemoteApp se espera si no se inicia ningún programa RemoteApp en la sesión dentro del límite de tiempo de espera, que es de dos minutos para Windows Server 2008.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ServerStartProgram(
  [in] BSTR         bstrExecutablePath,
  [in] BSTR         bstrFilePath,
  [in] BSTR         bstrWorkingDirectory,
  [in] VARIANT_BOOL vbExpandEnvVarInWorkingDirectoryOnServer,
  [in] BSTR         bstrArguments,
  [in] VARIANT_BOOL vbExpandEnvVarInArgumentsOnServer
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*bstrExecutablePath* \[ En\]
</dt> <dd>

Ruta de acceso del archivo ejecutable del programa RemoteApp en el servidor.

</dd> <dt>

*bstrFilePath* \[ En\]
</dt> <dd>

Ruta de acceso de un archivo que se abre en el servidor a través de una asociación de archivos, por ejemplo, "C: \\ \\ Documentos \\ \\MyReport.docx". Si especifica *bstrFilePath*, no debe especificar el *parámetro bstrExecutablePath* y viceversa. Solo debe especificar uno de los parámetros.

</dd> <dt>

*bstrWorkingDirectory* \[ En\]
</dt> <dd>

Directorio de trabajo en el servidor para el programa RemoteApp.

</dd> <dt>

*vbExpandEnvVarInWorkingDirectoryOnServer* \[ En\]
</dt> <dd>

Indica si el servidor debe expandir las variables de entorno en la ruta de acceso del directorio de trabajo. Establezca este parámetro en **VARIANT \_ TRUE si** la ruta de acceso del directorio de trabajo contiene variables de entorno o VARIANT **\_ FALSE** si la ruta de acceso del directorio de trabajo no contiene variables de entorno.

</dd> <dt>

*bstrArguments* \[ En\]
</dt> <dd>

Argumentos de línea de comandos para el programa RemoteApp especificados en *bstrExecutablePath*. Establezca esta opción **en NULL** si no se especifica *bstrExecutablePath.*

</dd> <dt>

*vbExpandEnvVarInArgumentsOnServer* \[ En\]
</dt> <dd>

Indica si el servidor debe expandir las variables de entorno en los argumentos de la línea de comandos. Establezca este parámetro en **VARIANT \_ TRUE si** los argumentos contienen variables de entorno o VARIANT **\_ FALSE** si los argumentos no contienen variables de entorno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ OK si** se realiza correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID ITSRemoteProgram se define como \_ FDD029F9-467A-4c49-8529-64B521DBD1B4<br/>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITSRemoteProgram2**](itsremoteprogram2.md)
</dt> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> <dt>

[**ITSRemoteProgram**](itsremoteprogram.md)
</dt> </dl>

 

 





