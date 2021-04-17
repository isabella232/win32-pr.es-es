---
description: El objeto SummaryInfo se usa para leer, crear y actualizar propiedades de documento desde la secuencia de información de Resumen de un objeto de almacenamiento.
ms.assetid: 296e90d2-84b8-4c9e-8716-be90f94294ee
title: SummaryInfo (objeto)
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
ms.openlocfilehash: 816a0ec4e307390edcb16d8e7096a7a4ef20c412
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105653731"
---
# <a name="summaryinfo-object"></a>SummaryInfo (objeto)

El objeto **SummaryInfo** se usa para leer, crear y actualizar propiedades de documento desde la [secuencia de información de Resumen](summary-information-stream.md) de un objeto de almacenamiento.

## <a name="members"></a>Miembros

El objeto **SummaryInfo** tiene estos tipos de miembros:

-   [Métodos](#methods)
-   [Propiedades](#properties)

### <a name="methods"></a>Métodos

El objeto **SummaryInfo** tiene estos métodos.



| Método                                 | Descripción                                                                                                                                    |
|:---------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**Persist**](summaryinfo-persist.md) | Da formato y escribe las propiedades previamente almacenadas en la [secuencia de información de Resumen](summary-information-stream.md)estándar.<br/> |



 

### <a name="properties"></a>Propiedades

El objeto **SummaryInfo** tiene estas propiedades.



| Propiedad                                                                             | Descripción                                                                                     |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------|
| [**Propiedad Property (objeto SummaryInfo)**](summaryinfo-summaryinfo.md)<br/> | Obtiene o establece el valor de la propiedad especificada en la secuencia de información de resumen.<br/> |
| [**PropertyCount**](summaryinfo-propertycount.md)<br/>                        | Indica el número actual de valores de propiedad en el objeto de información de resumen.<br/>   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Versión<br/> | Windows Installer 5,0 en Windows Server 2012, Windows 8, Windows Server 2008 R2 o Windows 7. Windows Installer 4,0 o Windows Installer 4,5 en Windows Server 2008 o Windows Vista. Windows Installer en Windows Server 2003 o Windows XP<br/> |
| Archivo DLL<br/>     | <dl> <dt>Msi.dll</dt> </dl>                                                                                                                                                                      |
| IID<br/>     | IID \_ ISummaryInfo se define como 000C109B-0000-0000-C000-000000000046<br/>                                                                                                                                                                         |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedad SummaryInformation (objeto Database)**](database-summaryinformation.md)
</dt> <dt>

[**Propiedad SummaryInformation (objeto Installer)**](installer-summaryinformation.md)
</dt> <dt>

[Ejemplos de scripting Windows Installer](windows-installer-scripting-examples.md)
</dt> </dl>

 

 




