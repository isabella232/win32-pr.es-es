---
title: Constantes BFT (Ntdsbcli.h)
description: Las constantes BFT se usan como marcas de bits para identificar distintos tipos de archivo en una copia de Active Directory Domain Services copia de seguridad.
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
ms.openlocfilehash: 3b5e9275e01b8c33d308b55b2638d4eaf186b8f5265834acc27acd2f146f0d09
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118024054"
---
# <a name="bft-constants"></a>Constantes de BFT

Las constantes BFT se usan como marcas de bits para identificar distintos tipos de archivo en una copia de Active Directory Domain Services copia de seguridad.

<dl> <dt>

<span id="BFT_LOG_DIRECTORY"></span><span id="bft_log_directory"></span>**DIRECTORIO DE REGISTRO \_ DE \_ BFT**
</dt> <dd> <dl> <dt>

0x20
</dt> <dt>



El archivo pertenece al directorio de registro.


</dt> </dl> </dd> <dt>

<span id="BFT_DATABASE_DIRECTORY"></span><span id="bft_database_directory"></span>**DIRECTORIO DE BASE \_ DE DATOS DE \_ BFT**
</dt> <dd> <dl> <dt>

0x40
</dt> <dt>



El archivo pertenece al directorio de base de datos.


</dt> </dl> </dd> <dt>

<span id="BFT_DIRECTORY"></span><span id="bft_directory"></span>**DIRECTORIO DE \_ BFT**
</dt> <dd> <dl> <dt>

0x80
</dt> <dt>



La ruta de acceso especificada es un directorio y no un nombre de archivo.


</dt> </dl> </dd> <dt>

<span id="BFT_LOG"></span><span id="bft_log"></span>**BFT \_ LOG**
</dt> <dd> <dl> <dt>

0x21
</dt> <dt>



Especifica un archivo de registro que pertenece al directorio de registro.


</dt> </dl> </dd> <dt>

<span id="BFT_LOG_DIR"></span><span id="bft_log_dir"></span>**BFT \_ LOG \_ DIR**
</dt> <dd> <dl> <dt>

0x22
</dt> <dt>



El archivo es la ruta de acceso del directorio de registro.


</dt> </dl> </dd> <dt>

<span id="BFT_CHECKPOINT_DIR"></span><span id="bft_checkpoint_dir"></span>**DIRECTORIO DE PUNTO DE COMPROBACIÓN DE BFT \_ \_**
</dt> <dd> <dl> <dt>

0x23
</dt> <dt>



El archivo es la ruta de acceso del directorio del punto de control.


</dt> </dl> </dd> <dt>

<span id="BFT_NTDS_DATABASE"></span><span id="bft_ntds_database"></span>**BFT \_ NTDS \_ DATABASE**
</dt> <dd> <dl> <dt>

0x44
</dt> <dt>



El archivo es una base de datos de servicio de directorio que pertenece al directorio de base de datos.


</dt> </dl> </dd> <dt>

<span id="BFT_PATCH_FILE"></span><span id="bft_patch_file"></span>**ARCHIVO DE \_ REVISIÓN DE \_ BFT**
</dt> <dd> <dl> <dt>

0x25
</dt> <dt>



El archivo es un archivo de revisión que pertenece al directorio de registro.


</dt> </dl> </dd> <dt>

<span id="BFT_UNKNOWN"></span><span id="bft_unknown"></span>**BFT \_ UNKNOWN**
</dt> <dd> <dl> <dt>

0x0F
</dt> <dt>



No se puede reconocer el archivo. El archivo no coincide con los nombres de archivo y los tipos de archivo conocidos.


</dt> </dl> </dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                        |
| Header<br/>                   | <dl> <dt>Ntdsbcli.h</dt> </dl> |



 

 





