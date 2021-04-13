---
title: Obtención de propiedades de cuentas
description: El objeto Accounting es uno de los objetos de la colección de controladores de solicitud.
ms.assetid: eb5c8606-d3f0-4c33-9035-7b7b1369cb0d
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9911397c1de3521ccb5a275405416d8b88c1fa6f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104420993"
---
# <a name="obtaining-accounting-properties"></a>Obtención de propiedades de cuentas

> [!Note]  
> Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.

 

El objeto Accounting es uno de los objetos de la colección de controladores de solicitud. El valor de enumeración para la colección de controladores de solicitud es la propiedad de la **\_ \_ \_ colección RequestHandler de IAS**. El nombre del controlador para el objeto Accounting es "Microsoft Accounting".

El código Visual Basic siguiente tiene acceso a las propiedades disponibles desde el controlador de objetos de contabilidad.


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



Para obtener acceso a las propiedades de cuentas mediante C++, primero obtenga la colección de controladores de solicitud. La [recuperación de una colección](/windows/desktop/Nps/sdo-retrieving-a-collection) contiene código de C++ que muestra cómo obtener una colección. El valor de enumeración para la colección de controladores de solicitud es la propiedad de la **\_ \_ \_ colección RequestHandler de IAS**. (Los valores correspondientes a las distintas colecciones de NPS se enumeran mediante el tipo de enumeración [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) ).

La colección de controladores de solicitud contiene un objeto denominado "Microsoft Accounting". Recupere este objeto de la colección. La sección [recuperar un objeto de una colección](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection) contiene código de C++ que muestra cómo obtener un objeto de una colección.

Una vez que tenga el objeto de contabilidad de Microsoft, obtenga una interfaz [**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo) para el objeto mediante [**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)). La sección [recuperar un SDO de usuarios](/windows/desktop/Nps/sdo-retrieving-a-user-sdo) contiene código de C++ que muestra cómo obtener una interfaz **ISdo** para un objeto. Después, puede usar el método [**ISdo:: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty) para obtener los valores de propiedad para el objeto de contabilidad de Microsoft.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Recuperación de una colección](/windows/desktop/Nps/sdo-retrieving-a-collection)
</dt> <dt>

[Recuperar un objeto de una colección](/windows/desktop/Nps/sdo-retrieving-an-object-from-a-collection)
</dt> <dt>

[Recuperación de un SDO de usuarios](/windows/desktop/Nps/sdo-retrieving-a-user-sdo)
</dt> <dt>

[**ISdo**](/windows/desktop/api/sdoias/nn-sdoias-isdo)
</dt> <dt>

[**IUnknown:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))
</dt> <dt>

[**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> </dl>

 

 