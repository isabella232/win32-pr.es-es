---
title: Constantes de WINBIO_DB (Winbio \_ Types. h)
description: Especifique la base de datos que se va a usar para un grupo de sistemas.
ms.assetid: 2cffa455-5834-4a35-b8d8-f9d1feddcaa1
topic_type:
- apiref
api_name:
- WINBIO_DB_DEFAULT
- WINBIO_DB_BOOTSTRAP
- WINBIO_DB_ONCHIP
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 20503e1dc3cd7b5e47651889dd9c67777614593c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150515"
---
# <a name="winbio_db-constants"></a>Constantes de WINBIO \_ dB

Las siguientes constantes se pueden usar al llamar a [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) para especificar la base de datos que se va a usar para un grupo de sistema.



| Constante                                                                                                                                                                         | Descripción                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DB_DEFAULT"></span><span id="winbio_db_default"></span><dl> <dt>**\_ \_ valor predeterminado de la base de WINBIO**</dt> </dl>       | Cada unidad biométrica del grupo de sensores utiliza la base de datos predeterminada especificada en la configuración de unidad biométrica predeterminada.<br/>                                                                   |
| <span id="WINBIO_DB_BOOTSTRAP"></span><span id="winbio_db_bootstrap"></span><dl> <dt>**BOOTSTRAP de WINBIO \_ dB \_**</dt> </dl> | Se puede usar para escenarios antes de iniciar Windows. Normalmente, la base de datos forma parte del chip del sensor o forma parte del BIOS y solo se puede usar para la inscripción y eliminación de plantillas.<br/> |
| <span id="WINBIO_DB_ONCHIP"></span><span id="winbio_db_onchip"></span><dl> <dt>**WINBIO \_ dB en \_ chip**</dt> </dl>          | La base de datos reside en el chip del sensor.<br/>                                                                                                                                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ Types. h (incluye Winbio. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





