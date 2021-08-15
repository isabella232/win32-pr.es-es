---
title: Obtener propiedades de contabilidad
description: El objeto de contabilidad es uno de los objetos de la colección Controladores de solicitudes.
ms.assetid: eb5c8606-d3f0-4c33-9035-7b7b1369cb0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 77390a6aa67e946de6d69dd3d1bc28a76907b7ad31b497d4921c7a2d7493c328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118361733"
---
# <a name="obtaining-accounting-properties"></a>Obtener propiedades de contabilidad

> [!Note]  
> El nombre del Servicio de autenticación de Internet (IAS) se ha cambiado a Servidor de directivas de red (NPS) a partir Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. A lo largo del texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones a las que se hizo referencia originalmente como IAS.

 

El objeto de contabilidad es uno de los objetos de la colección Controladores de solicitudes. El valor de enumeración de la colección de controladores de solicitudes **es PROPERTY \_ IAS \_ REQUESTHANDLERS \_ COLLECTION**. El nombre del controlador para el objeto de contabilidad es "Microsoft Accounting".

El código Visual Basic acceso a las propiedades disponibles desde el controlador de objetos de contabilidad.


```VB
Set sdoRequestHandler = sdoCollRequestHandlers.Item("Microsoft Accounting")
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_ACCOUNTING_INTERIM)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_AUTHENTICATION)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_FILE_DIRECTORY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_IAS1_FORMAT)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_FREQUENCY)
vtTemp = sdoRequestHandler.GetProperty(PROPERTY_ACCOUNTING_LOG_OPEN_NEW_SIZE)
```



Para acceder a las propiedades de contabilidad mediante C++, obtenga primero la colección de controladores de solicitudes. Recuperar [una colección contiene](/windows/desktop/Nps/sdo-retrieving-a-collection) código de C++ que muestra cómo obtener una colección. El valor de enumeración de la colección de controladores de solicitudes **es PROPERTY \_ IAS \_ REQUESTHANDLERS \_ COLLECTION**. (Los valores correspondientes a las distintas colecciones NPS se enumeran mediante el [**tipo de enumeración IASPROPERTIES).**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)

La colección de controladores de solicitudes contiene un objeto denominado "Microsoft Accounting". Recupere este objeto de la colección. La sección [Recuperar un objeto de una colección](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) contiene código de C++ que muestra cómo obtener un objeto de una colección.

Una vez que tenga el objeto Microsoft Accounting, obtenga una interfaz [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) para el objeto mediante [**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). La sección [Recuperación de un SDO de](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) usuario contiene código de C++ que muestra cómo obtener una **interfaz ISdo** para un objeto . A continuación, puede usar [**el método ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) para obtener valores de propiedad para el objeto Microsoft Accounting.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recuperar una colección](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[Recuperar un objeto de una colección](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection)
</dt> <dt>

[Recuperar un SDO de usuario](/windows/desktop/Nps/sdo-retrieving-a-user-sdo)
</dt> <dt>

[**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

[**IUnknown::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
</dt> <dt>

[**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 