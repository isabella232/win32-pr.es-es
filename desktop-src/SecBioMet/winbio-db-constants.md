---
title: WINBIO_DB constantes (Winbio \_ types.h)
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
ms.openlocfilehash: 0a9d8392fd38e9d53588002c8aeab688ffc8b76efced83819318d9c6b6c2b721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867985"
---
# <a name="winbio_db-constants"></a>Constantes de base de datos WINBIO \_

Las siguientes constantes se pueden usar al llamar a [**WinBioOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioopensession) para especificar la base de datos que se va a usar para un grupo de sistemas.



| Constante                                                                                                                                                                         | Descripción                                                                                                                                                                                          |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DB_DEFAULT"></span><span id="winbio_db_default"></span><dl> <dt>**VALOR PREDETERMINADO DE WINBIO \_ DB \_**</dt> </dl>       | Cada unidad biométrica del grupo de sensores usa la base de datos predeterminada especificada en la configuración de unidad biométrica predeterminada.<br/>                                                                   |
| <span id="WINBIO_DB_BOOTSTRAP"></span><span id="winbio_db_bootstrap"></span><dl> <dt>**ARRANQUE DE WINBIO \_ DB \_**</dt> </dl> | Se puede usar para escenarios antes de iniciar Windows. Normalmente, la base de datos forma parte del chip del sensor o forma parte del BIOS y solo se puede usar para la inscripción y eliminación de plantillas.<br/> |
| <span id="WINBIO_DB_ONCHIP"></span><span id="winbio_db_onchip"></span><dl> <dt>**WINBIO \_ DB \_ ONCHIP**</dt> </dl>          | La base de datos reside en el chip del sensor.<br/>                                                                                                                                                  |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Header<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





