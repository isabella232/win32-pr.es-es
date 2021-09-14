---
title: WINBIO_BIR_QUALITY constantes (Winbio \_ types.h)
description: Especifique la calidad relativa de los datos biométricos en bir si no se ha especificado un valor entero de 0 a 100.
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071160"
---
# <a name="winbio_bir_quality-constants"></a>Constantes DE \_ CALIDAD DE BIR DE WINBIO \_

El miembro **DataQuality** de la estructura [**WINBIO \_ BIR \_ HEADER**](winbio-bir-header.md) usa las marcas siguientes para especificar la calidad relativa de los datos biométricos en bir si no se ha especificado un valor entero de 0 a 100.



| Constante o valor                                                                                                                                                                                                                                                                       | Descripción                                                                                       |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------|
| <span id="WINBIO_DATA_QUALITY_NOT_SET"></span><span id="winbio_data_quality_not_set"></span><dl> <dt>**WINBIO \_ CALIDAD \_ DE DATOS NO \_ \_ ESTABLECIDA**</dt> <dt> EN 1</dt> </dl>                   | Las medidas de calidad son compatibles con el creador de BIR, pero no se establece ningún valor en la BIR.<br/> |
| <span id="WINBIO_DATA_QUALITY_NOT_SUPPORTED"></span><span id="winbio_data_quality_not_supported"></span><dl> <dt>**WINBIO \_ CALIDAD \_ DE DATOS NO \_ \_ ADMITIDA**</dt> <dt> 2</dt> </dl> | Las medidas de calidad no son compatibles con el creador de BIR.<br/>                             |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                                       |
| Encabezado<br/>                   | <dl> <dt>Winbio \_ types.h (incluir Winbio.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Constantes de aplicación cliente](client-application-constants.md)
</dt> </dl>

 

 





