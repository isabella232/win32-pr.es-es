---
description: Accede a los datos almacenados en el catálogo de COM+.
ms.assetid: d77123f6-9821-4c80-860c-5f1feaca7987
title: Clase COMAdminCatalog (ComAdmin.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COMAdminCatalog
api_type:
- COM
api_location:
- ComAdmin.Idl
ms.openlocfilehash: 8be3f0f3f9aa59c2199c50b73b8a4d4488b0c9a65d3e0679b65350d6b8b07fd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119128997"
---
# <a name="comadmincatalog-class"></a>COMAdminCatalog (clase)

Accede a los datos almacenados en el catálogo de COM+.

## <a name="when-to-implement"></a>Cuándo implementar

COM+implementa esta clase.



| Requisito | Value |
|------------|-------------------------------------------------------------------------------------------------------------------|
| CLSID      | CLSID \_ COMAdminCatalog                                                                                            |
| ProgID     | L"COMAdmin.COMAdminCatalog"                                                                                       |
| Interfaces | [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)<br/> [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)<br/> |



 

## <a name="when-to-use"></a>Cuándo se usa

Los objetos creados a partir de la **clase COMAdminCatalog** se usan para iniciar el acceso mediante programación a los datos de configuración de COM+ almacenados en el catálogo de COM+. Esta información subyace a las carpetas y elementos del árbol de consola de la herramienta de administración servicios de componentes. La **clase COMAdminCatalog** permite acceder a colecciones del catálogo, instalar aplicaciones y componentes com+ , iniciar y detener servicios, y conectarse a servidores remotos y administrarlo.

Las carpetas de la herramienta de administración Servicios de componentes corresponden a colecciones del catálogo, que se pueden representar mediante objetos creados a partir de la [**clase COMAdminCatalogCollection.**](comadmincatalogcollection.md) Los elementos de las carpetas corresponden a elementos de las colecciones, que se pueden representar mediante objetos creados a partir de la [**clase COMAdminCatalogObject.**](comadmincatalogobject.md)

No todas las colecciones y elementos expuestos a través de [**COMAdminCatalogCollection**](comadmincatalogcollection.md) y [**COMAdminCatalogObject**](comadmincatalogobject.md) están disponibles en la herramienta de administración servicios de componentes.

Para obtener información sobre colecciones específicas y sus propiedades, vea [Colecciones de administración de COM+.](com--administration-collections.md)

Para obtener una introducción a la administración mediante programación de COM+, vea [Automatización de la administración de COM+.](automating-com--administration.md)

## <a name="remarks"></a>Comentarios

Para crear este objeto, llame a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Para usar esta clase de Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de administrador de COM+. Un objeto COMAdminCatalog se puede declarar mediante "COMAdmin.COMAdminCatalog" como nombre de clase.

En COM+ 1.5, publicado con Windows XP, la clase **COMAdminCatalog** implementa la [**interfaz ICOMAdminCatalog2.**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) Sin embargo, en COM+ 1.0, publicado con Windows 2000, la clase **COMAdminCatalog** implementa solo la [**interfaz ICOMAdminCatalog.**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>ComAdmin.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>ComAdmin.Idl</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**COMAdminCatalogCollection**](comadmincatalogcollection.md)
</dt> <dt>

[**COMAdminCatalogObject**](comadmincatalogobject.md)
</dt> <dt>

[**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)
</dt> <dt>

[**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)
</dt> </dl>

 

