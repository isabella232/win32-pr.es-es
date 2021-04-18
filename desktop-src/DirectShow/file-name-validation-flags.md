---
description: Estas marcas especifican el comportamiento del localizador de medios.
ms.assetid: 60afb2e8-cdd1-493e-8fc8-6fa581720b8d
title: Marcas de validación de nombre de archivo (QEDIT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SFN_VALIDATEF_CHECK
- SFN_VALIDATEF_POPUP
- SFN_VALIDATEF_TELLME
- SFN_VALIDATEF_REPLACE
- SFN_VALIDATEF_USELOCAL
- SFN_VALIDATEF_NOFIND
- SFN_VALIDATEF_IGNOREMUTED
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: d8930241be0306c637bcab36207fec1de2e489c9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679559"
---
# <a name="file-name-validation-flags"></a>Marcas de validación de nombre de archivo

\[En desuso. Esta API se puede quitar de las versiones futuras de Windows.\]

Estas marcas especifican el comportamiento del localizador de medios.



| Constante o valor                                                                                                                                                                                                                                               | Descripción                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFN_VALIDATEF_CHECK"></span><span id="sfn_validatef_check"></span><dl> <dt>**SFN \_ VALIDATEF \_ comprobar**</dt> <dt>0x01</dt> </dl>                   | Compruebe la validez de los nombres de archivo. Debe establecer esta marca para validar los nombres de archivo. En caso contrario, los demás marcadores no tienen ningún efecto.<br/>                                                                                            |
| <span id="SFN_VALIDATEF_POPUP"></span><span id="sfn_validatef_popup"></span><dl> <dt>**SFN \_ VALIDATEF \_ emergente**</dt> <dt>0x02</dt> </dl>                   | Si no se encuentra un archivo, muestra un cuadro de diálogo Abrir archivo para el usuario final.<br/>                                                                                                                                         |
| <span id="SFN_VALIDATEF_TELLME"></span><span id="sfn_validatef_tellme"></span><dl> <dt>**SFN \_ VALIDATEF \_ TELLME**</dt> <dt>0x04</dt> </dl>                | Si se encuentra un archivo que falta, muestre brevemente un cuadro de mensaje con el nombre y la ubicación del archivo. Esta marca es principalmente útil para fines de prueba; es probable que el cuadro de mensaje no sea adecuado para un producto comercial.<br/> |
| <span id="SFN_VALIDATEF_REPLACE"></span><span id="sfn_validatef_replace"></span><dl> <dt>**SFN \_ VALIDATEF \_ reemplazar**</dt> <dt>0x08</dt> </dl>             | Si se encuentra un archivo que falta, actualice el nombre del objeto de origen. (Solo es válido en el método [**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md) ).<br/>                                         |
| <span id="SFN_VALIDATEF_USELOCAL"></span><span id="sfn_validatef_uselocal"></span><dl> <dt>**SFN \_ VALIDATEF \_ USELOCAL**</dt> <dt>0x10</dt> </dl>          | Use siempre un archivo local, incluso si existe una versión del archivo en la red.<br/>                                                                                                                                       |
| <span id="SFN_VALIDATEF_NOFIND"></span><span id="sfn_validatef_nofind"></span><dl> <dt>**SFN \_ VALIDATEF \_ NoFind**</dt> <dt>0x20</dt> </dl>                | No busque archivos que faltan. Los nombres de archivo siguen validados si se establece la \_ marca de comprobación de VALIDATEF de SFN \_ .<br/>                                                                                                          |
| <span id="SFN_VALIDATEF_IGNOREMUTED"></span><span id="sfn_validatef_ignoremuted"></span><dl> <dt>**SFN \_ VALIDATEF \_ IGNOREMUTED**</dt> <dt>0x40</dt> </dl> | Omitir objetos de origen silenciados. (Solo es válido en el método [**IAMTimeline:: ValidateSourceNames**](iamtimeline-validatesourcenames.md) ).<br/>                                                                                |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>QEDIT. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md)
</dt> <dt>

[**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md)
</dt> </dl>

 

 




