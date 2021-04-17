---
description: Obtiene acceso a los datos que se almacenan en el catálogo de COM+.
ms.assetid: d77123f6-9821-4c80-860c-5f1feaca7987
title: Clase COMAdminCatalog (COMAdmin. h)
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
ms.openlocfilehash: fa6e71d13f5a3d157bd3ce1035d0616dc1e5a519
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496463"
---
# <a name="comadmincatalog-class"></a>Clase COMAdminCatalog

Obtiene acceso a los datos que se almacenan en el catálogo de COM+.

## <a name="when-to-implement"></a>Cuándo implementar

Esta clase se implementa mediante COM+.



| Requisito | Value |
|------------|-------------------------------------------------------------------------------------------------------------------|
| CLSID      | CLSID \_ COMAdminCatalog                                                                                            |
| ProgID     | L "COMAdmin. COMAdminCatalog"                                                                                       |
| Interfaces | [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog)<br/> [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2)<br/> |



 

## <a name="when-to-use"></a>Cuándo se usa

Los objetos creados a partir de la clase **COMAdminCatalog** se usan para comenzar el acceso mediante programación a los datos de configuración de com+ almacenados en el catálogo de com+. Esta información se basa en las carpetas y los elementos en el árbol de consola de la herramienta de administración de servicios de componentes. La clase **COMAdminCatalog** permite obtener acceso a las colecciones del catálogo, instalar aplicaciones y componentes com+, iniciar y detener servicios, y conectarse a los servidores remotos y administrarlos.

Las carpetas de la herramienta de administración de servicios de componentes se corresponden con las recopilaciones del catálogo, que se pueden representar mediante los objetos creados a partir de la clase [**COMAdminCatalogCollection**](comadmincatalogcollection.md) . Los elementos de las carpetas corresponden a los elementos de las colecciones, que puede representar con los objetos creados a partir de la clase [**COMAdminCatalogObject**](comadmincatalogobject.md) .

No todas las colecciones y elementos expuestos a través de [**COMAdminCatalogCollection**](comadmincatalogcollection.md) y [**COMAdminCatalogObject**](comadmincatalogobject.md) están disponibles en la herramienta de administración de servicios de componentes.

Para obtener información sobre colecciones específicas y sus propiedades, consulte [colecciones de administración de com+](com--administration-collections.md).

Para obtener una introducción a la administración mediante programación de COM+, vea [automatizar la administración de com+](automating-com--administration.md).

## <a name="remarks"></a>Observaciones

Para crear este objeto, llame a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).

Para usar esta clase desde Microsoft Visual Basic, agregue una referencia a la biblioteca de tipos de administración de COM+. Un objeto COMAdminCatalog se puede declarar mediante "COMAdmin. COMAdminCatalog" como nombre de clase.

En COM+ 1,5, lanzado con Windows XP, la clase **COMAdminCatalog** implementa la interfaz [**ICOMAdminCatalog2**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog2) . Sin embargo, en COM+ 1,0, lanzado con Windows 2000, la clase **COMAdminCatalog** solo implementa la interfaz [**ICOMAdminCatalog**](/windows/desktop/api/ComAdmin/nn-comadmin-icomadmincatalog) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                              |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                    |
| Encabezado<br/>                   | <dl> <dt>COMAdmin. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>COMAdmin. idl</dt> </dl> |



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

 

