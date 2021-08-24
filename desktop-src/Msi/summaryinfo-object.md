---
description: El objeto SummaryInfo se usa para leer, crear y actualizar las propiedades del documento desde el flujo de información de resumen de un objeto de almacenamiento.
ms.assetid: 296e90d2-84b8-4c9e-8716-be90f94294ee
title: Objeto SummaryInfo
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SummaryInfo
api_type:
- COM
api_location:
- Msi.dll
ms.openlocfilehash: 3efdc009f40f0bce67559d185afb4cba1289c00fc1d7771a43d392601220dbae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120039595"
---
# <a name="summaryinfo-object"></a>Objeto SummaryInfo

El **objeto SummaryInfo** se usa para leer, crear y actualizar las propiedades del documento desde el flujo de información [de resumen](summary-information-stream.md) de un objeto de almacenamiento.

## <a name="members"></a>Miembros

El **objeto SummaryInfo** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El **objeto SummaryInfo** tiene estos métodos.



| Método                                 | Descripción                                                                                                                                    |
|:---------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Persist**](summaryinfo-persist.md) | Da formato y escribe las propiedades almacenadas previamente en el flujo de información [de resumen estándar.](summary-information-stream.md)<br/> |



 

### <a name="properties"></a>Propiedades

El **objeto SummaryInfo** tiene estas propiedades.



| Propiedad                                                                             | Descripción                                                                                     |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**Propiedad Property (objeto SummaryInfo)**](summaryinfo-summaryinfo.md)<br/> | Obtiene o establece el valor de la propiedad especificada en el flujo de información de resumen.<br/> |
| [**PropertyCount**](summaryinfo-propertycount.md)<br/>                        | Indica el número actual de valores de propiedad en el objeto de información de resumen.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Instalador 5.0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Instalador 4.0 o Windows Installer 4.5 en Windows Server 2008 o Windows Vista. Windows Instalador en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID ISummaryInfo se define como \_ 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**SummaryInformation (propiedad, objeto Database)**](database-summaryinformation.md)
</dt> <dt>

[**Propiedad SummaryInformation (objeto Installer)**](installer-summaryinformation.md)
</dt> <dt>

[Windows Ejemplos de scripting del instalador](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




