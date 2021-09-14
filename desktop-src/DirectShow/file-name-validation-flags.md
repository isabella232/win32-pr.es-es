---
description: Estas marcas especifican el comportamiento del localizador de medios.
ms.assetid: 60afb2e8-cdd1-493e-8fc8-6fa581720b8d
title: Marcas de validación de nombres de archivo (Qedit.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255170"
---
# <a name="file-name-validation-flags"></a>Marcas de validación de nombre de archivo

\[Obsoleto. Esta API puede quitarse de futuras versiones de Windows.\]

Estas marcas especifican el comportamiento del localizador de medios.



| Constante o valor                                                                                                                                                                                                                                               | Descripción                                                                                                                                                                                                                    |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="SFN_VALIDATEF_CHECK"></span><span id="sfn_validatef_check"></span><dl> <dt>**SFN \_ ValidateF \_ CHECK**</dt> <dt>0x01</dt> </dl>                   | Compruebe la validez de los nombres de archivo. Debe establecer esta marca para validar los nombres de archivo. Si no es así, las demás marcas no tienen ningún efecto.<br/>                                                                                            |
| <span id="SFN_VALIDATEF_POPUP"></span><span id="sfn_validatef_popup"></span><dl> <dt>**SFN \_ Cuadro emergente \_ VALIDATEF**</dt> <dt>0x02</dt> </dl>                   | Si no se encuentra un archivo, muestre un cuadro de diálogo Abrir archivo para el usuario final.<br/>                                                                                                                                         |
| <span id="SFN_VALIDATEF_TELLME"></span><span id="sfn_validatef_tellme"></span><dl> <dt>**SFN \_ ValidateF \_ TELLME**</dt> <dt>0x04</dt> </dl>                | Si se encuentra un archivo que falta, muestre brevemente un cuadro de mensaje con el nombre y la ubicación del archivo. Esta marca es principalmente útil para fines de prueba; el cuadro de mensaje probablemente no sea adecuado para un producto minorista.<br/> |
| <span id="SFN_VALIDATEF_REPLACE"></span><span id="sfn_validatef_replace"></span><dl> <dt>**SFN \_ ValidateF \_ REPLACE**</dt> <dt>0x08</dt> </dl>             | Si se encuentra un archivo que falta, actualice el nombre del objeto de origen. (Solo es válido en el [**método IAMTimeline::ValidateSourceNames).**](iamtimeline-validatesourcenames.md)<br/>                                         |
| <span id="SFN_VALIDATEF_USELOCAL"></span><span id="sfn_validatef_uselocal"></span><dl> <dt>**SFN \_ VALIDATEF \_ USELOCAL**</dt> <dt>0x10</dt> </dl>          | Use siempre un archivo local, incluso si existe una versión del archivo en la red.<br/>                                                                                                                                       |
| <span id="SFN_VALIDATEF_NOFIND"></span><span id="sfn_validatef_nofind"></span><dl> <dt>**SFN \_ ValidateF \_ NOFIND**</dt> <dt>0x20</dt> </dl>                | No busque los archivos que faltan. Los nombres de archivo se siguen validando si establece la \_ marca VALIDATEF CHECK de SFN. \_<br/>                                                                                                          |
| <span id="SFN_VALIDATEF_IGNOREMUTED"></span><span id="sfn_validatef_ignoremuted"></span><dl> <dt>**SFN \_ VALIDATEF \_ IGNOREMUTED**</dt> <dt>0x40</dt> </dl> | Omitir objetos de origen muted. (Solo es válido en el [**método IAMTimeline::ValidateSourceNames).**](iamtimeline-validatesourcenames.md)<br/>                                                                                |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMediaLocator::FindMediaFile**](imedialocator-findmediafile.md)
</dt> <dt>

[**IRenderEngine::SetSourceNameValidation**](irenderengine-setsourcenamevalidation.md)
</dt> </dl>

 

 




