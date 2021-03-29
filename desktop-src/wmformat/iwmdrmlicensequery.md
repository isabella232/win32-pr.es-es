---
title: Interfaz IWMDRMLicenseQuery
description: La interfaz IWMDRMLicenseQuery permite que las aplicaciones consulten los derechos y el estado de la licencia de un archivo protegido.
ms.assetid: 4ec8ff9f-0acb-4389-8995-65f24736491b
keywords:
- Interfaz IWMDRMLicenseQuery formato de Windows Media
- Interfaz IWMDRMLicenseQuery formato de Windows Media, descrito
topic_type:
- apiref
api_name:
- IWMDRMLicenseQuery
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 6463f405bf50d4d4ecb037dc542e3af0e5b7df46
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103792687"
---
# <a name="iwmdrmlicensequery-interface"></a>Interfaz IWMDRMLicenseQuery

La interfaz **IWMDRMLicenseQuery** permite que las aplicaciones consulten los derechos y el estado de la licencia de un archivo protegido. Esta interfaz usa el identificador de clave para realizar consultas en el almacén de licencias local.

Para obtener una instancia de esta interfaz, llame a [**IWMDRMProvider:: CreateObject**](iwmdrmprovider-createobject.md). Pase el **IID \_ IWMDRMLicenseQuery** como parámetro *riid* .

## <a name="members"></a>Miembros

La interfaz **IWMDRMLicenseQuery** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **IWMDRMLicenseQuery** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **IWMDRMLicenseQuery** tiene estos métodos.



| Método                                                                                | Descripción                                                                                      |
|:--------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------|
| [**QueryActionAllowed**](iwmdrmlicensequery-queryactionallowed.md)                   | Consulta el almacén de licencias local para obtener los permisos para realizar acciones por identificador de clave.<br/>         |
| [**QueryLicenseState**](iwmdrmlicensequery-querylicensestate.md)                     | Consulta el almacén de licencias local para los datos de estado de licencia por identificador de clave y derechos específicos.<br/> |
| [**SetActionAllowedQueryParams**](iwmdrmlicensequery-setactionallowedqueryparams.md) | Establece parámetros de entorno para mejorar la precisión de las consultas de licencia.<br/>             |



 

## <a name="remarks"></a>Observaciones

Los métodos de **IWMDRMLicenseQuery** no proporcionan información sobre licencias individuales. En su lugar, los datos de la licencia se agregan mediante el subsistema DRM antes de que se devuelvan los resultados de la consulta.

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Interfaces**](drm-interfaces.md)
</dt> </dl>

 

