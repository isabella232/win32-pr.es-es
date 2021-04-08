---
title: Constantes BFT (Ntdsbcli. h)
description: Las constantes BFT se usan como marcas de bits para identificar distintos tipos de archivo en una copia de seguridad de Active Directory Domain Services.
ms.assetid: 3658a657-d9e3-4fbf-9120-4b0205b81a36
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- BFT_LOG_DIRECTORY
- BFT_DATABASE_DIRECTORY
- BFT_DIRECTORY
- BFT_LOG
- BFT_LOG_DIR
- BFT_CHECKPOINT_DIR
- BFT_NTDS_DATABASE
- BFT_PATCH_FILE
- BFT_UNKNOWN
api_location:
- Ntdsbcli.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9607b5e61e5689d8895b39a11aa7e813fc7fcbe6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996236"
---
# <a name="bft-constants"></a>Constantes de BFT

Las constantes BFT se usan como marcas de bits para identificar distintos tipos de archivo en una copia de seguridad de Active Directory Domain Services.

<dl> <dt>

<span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**\_Directorio de registro de BFT \_**
</dt> <dd> <dl> <dt>

0x20
</dt> <dt>



El archivo pertenece al directorio de registro.


</dt> </dl> </dd> <dt>

<span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**\_Directorio de base de datos BFT \_**
</dt> <dd> <dl> <dt>

0x40
</dt> <dt>



El archivo pertenece al directorio de la base de datos.


</dt> </dl> </dd> <dt>

<span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**\_directorio BFT**
</dt> <dd> <dl> <dt>

0x80
</dt> <dt>



La ruta de acceso especificada es un directorio y no un nombre de archivo.


</dt> </dl> </dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>**registro de BFT \_**
</dt> <dd> <dl> <dt>

0x21
</dt> <dt>



Especifica un archivo de registro que pertenece al directorio de registro.


</dt> </dl> </dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**DIR. de registro de BFT \_ \_**
</dt> <dd> <dl> <dt>

0x22
</dt> <dt>



El archivo es la ruta de acceso del directorio de registro.


</dt> </dl> </dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**DIR. de punto de BFT \_ \_**
</dt> <dd> <dl> <dt>

0x23
</dt> <dt>



El archivo es la ruta de acceso del directorio Checkpoint.


</dt> </dl> </dd> <dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**\_base de \_ datos Ntds BFT**
</dt> <dd> <dl> <dt>

0X44
</dt> <dt>



El archivo es una base de datos del servicio de directorio que pertenece al directorio de la base de datos.


</dt> </dl> </dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**\_archivo de revisión BFT \_**
</dt> <dd> <dl> <dt>

0x25
</dt> <dt>



El archivo es un archivo de revisión que pertenece al directorio de registro.


</dt> </dl> </dd> <dt>

<span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**BFT \_ desconocido**
</dt> <dd> <dl> <dt>

0x0F
</dt> <dt>



No se reconoce el archivo. El archivo no coincide con los nombres de archivo y los tipos de archivo conocidos.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Ntdsbcli. h</dt> </dl> |



 

 





