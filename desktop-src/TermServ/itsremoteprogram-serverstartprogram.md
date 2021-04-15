---
title: ITSRemoteProgram ServerStartProgram, método
description: Especifica un programa RemoteApp para iniciarse en la sesión remota.
ms.assetid: 5fb251bf-4832-4e35-b372-23418c280350
ms.tgt_platform: multiple
keywords:
- Método ServerStartProgram Servicios de Escritorio remoto
- Método ServerStartProgram Servicios de Escritorio remoto, interfaz ITSRemoteProgram
- Interfaz ITSRemoteProgram Servicios de Escritorio remoto, método ServerStartProgram
- Método ServerStartProgram Servicios de Escritorio remoto, interfaz ITSRemoteProgram2
- Interfaz ITSRemoteProgram2 Servicios de Escritorio remoto, método ServerStartProgram
- Método ServerStartProgram Servicios de Escritorio remoto, interfaz ITSRemoteProgram3
- Interfaz ITSRemoteProgram3 Servicios de Escritorio remoto, método ServerStartProgram
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
ms.openlocfilehash: 1f18917eeb2eb3c60c1a35683b20f7e4604eddde
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534431"
---
# <a name="itsremoteprogramserverstartprogram-method"></a>ITSRemoteProgram:: ServerStartProgram (método)

Especifica un programa RemoteApp para iniciarse en la sesión remota. Esta función se debe invocar en una sesión conectada (después de que se reciba la notificación conectada a la sesión en el cliente). Se puede iniciar cualquier número de Programas RemoteApp en una sesión. Se agotará el tiempo de espera de una sesión de RemoteApp si no se inicia ningún programa RemoteApp en la sesión en el límite de tiempo de espera, que es de dos minutos para Windows Server 2008.

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

*bstrExecutablePath* \[ de\]
</dt> <dd>

La ruta de acceso del archivo ejecutable del programa RemoteApp en el servidor.

</dd> <dt>

*bstrFilePath* \[ de\]
</dt> <dd>

La ruta de acceso de un archivo que se va a abrir en el servidor a través de una asociación de archivo, por ejemplo "C: \\ \\ documents \\ \\MyReport.docx". Si especifica *bstrFilePath*, no debe especificar el parámetro *bstrExecutablePath* y viceversa. Solo debe especificar uno de los parámetros.

</dd> <dt>

*bstrWorkingDirectory* \[ de\]
</dt> <dd>

El directorio de trabajo en el servidor para el programa RemoteApp.

</dd> <dt>

*vbExpandEnvVarInWorkingDirectoryOnServer* \[ de\]
</dt> <dd>

Indica si el servidor debe expandir las variables de entorno en la ruta de acceso del directorio de trabajo. Establezca este parámetro en **Variant \_ true** si la ruta de acceso del directorio de trabajo contiene variables de entorno o **Variant \_ false** si la ruta de acceso del directorio de trabajo no contiene variables de entorno.

</dd> <dt>

*bstrArguments* \[ de\]
</dt> <dd>

Argumentos de la línea de comandos para el programa RemoteApp que se especifican en *bstrExecutablePath*. Establézcalo en **null** si no se especifica *bstrExecutablePath* .

</dd> <dt>

*vbExpandEnvVarInArgumentsOnServer* \[ de\]
</dt> <dd>

Indica si el servidor debe expandir las variables de entorno en los argumentos de la línea de comandos. Establezca este parámetro en **Variant \_ true** si los argumentos contienen variables de entorno o **Variant \_ false** si los argumentos no contienen variables de entorno.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **S \_ correcto** si se realiza correctamente.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ ITSRemoteProgram se define como FDD029F9-467A-4c49-8529-64B521DBD1B4<br/>    |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITSRemoteProgram2**](itsremoteprogram2.md)
</dt> <dt>

[**ITSRemoteProgram3**](itsremoteprogram3.md)
</dt> <dt>

[**ITSRemoteProgram**](itsremoteprogram.md)
</dt> </dl>

 

 





