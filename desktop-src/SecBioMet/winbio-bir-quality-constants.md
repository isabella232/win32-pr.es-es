---
title: Constantes de WINBIO_BIR_QUALITY (Winbio \_ Types. h)
description: Especifique la calidad relativa de los datos biométricos en el BIR si no se ha especificado un valor entero de 0 a 100.
ms.assetid: A42AA21B-9AA5-4DB6-B58F-0776BEC63E6C
topic_type:
- apiref
api_name:
- WINBIO_DATA_QUALITY_NOT_SET
- WINBIO_DATA_QUALITY_NOT_SUPPORTED
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1eb0881672c9e3bf51214cff93cb3f68d802b04
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151123"
---
# <a name="winbio_bir_quality-constants"></a>Constantes de calidad de WINBIO \_ Bir \_

El miembro de **calidad** de datos de la estructura de [**\_ \_ encabezado WINBIO Bir**](winbio-bir-header.md) utiliza las marcas siguientes para especificar la calidad relativa de los datos biométricos en Bir si no se ha especificado un valor entero de 0 a 100.



| Constante o valor                                                                                                                                                                                                                                                                       | Descripción                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <dt>**WINBIO \_ Calidad de datos \_ \_ no \_ establecida**</dt> <dt> 1</dt> </dl>                   | El creador de BIR admite las medidas de calidad, pero no se establece ningún valor en BIR.<br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <dt>**WINBIO \_ Calidad de datos \_ \_ no \_ admitida**</dt> <dt> 2</dt> </dl> | El creador de BIR no admite las medidas de calidad.<br/>                             |



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

 

 





