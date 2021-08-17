---
title: Recuperar una colección
description: Recuperar una colección
ms.assetid: b9090ad5-564c-4f48-b7bd-24617d582d2e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 343f00ee28475d1e6180646a0e548c18d51701afed587c99582dad7dc60d094c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119063315"
---
# <a name="retrieving-a-collection"></a>Recuperar una colección

> [!Note]  
> El nombre del Servicio de autenticación de Internet (IAS) se cambió a Servidor de directivas de red (NPS) a partir Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. A lo largo del texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones a las que se hizo referencia originalmente como IAS.

 

El código siguiente recupera la colección de clientes para el servidor de directivas de red.


```C++
// Retrieve the clients collection 
   HRESULT hr;
   CComPtr<ISdo>  pSdo;
   hr = pSdoServiceControl->QueryInterface(
      __uuidof(ISdo),
      (void**) &pSdo
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // First Retrieve the protocols collection
   //
   _variant_t  vtProtocolsCollection;
   hr = pSdo->GetProperty(
      PROPERTY_IAS_PROTOCOLS_COLLECTION,
      &vtProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Get the ISdoCollection interface 
   // for the object.
   //
   CComPtr<ISdoCollection>  pProtocolsCollection;
   hr = vtProtocolsCollection.pdispVal->QueryInterface(
      __uuidof(ISdoCollection), 
      (void **) &pProtocolsCollection
   );
   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Then retrieve the RADIUS protocol
   //
   CComPtr<IDispatch> pRadiusDispatch;
   _variant_t  vtProtocolName = L"Microsoft Radius Protocol";
   hr = pProtocolsCollection->Item(&vtProtocolName, &pRadiusDispatch);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdo> pRadiusSdo;
   hr = pRadiusDispatch->QueryInterface(      
      __uuidof(ISdo), 
      (void **) &pRadiusSdo
   );

   if (FAILED(hr))
   {
      return hr;
   }

   //
   // Then retrieve the clients collection
   //
   _variant_t  vtClientsCollection;
   hr = pRadiusSdo->GetProperty(PROPERTY_RADIUS_CLIENTS_COLLECTION, &vtClientsCollection);
   if (FAILED(hr))
   {
      return hr;
   }

   CComPtr<ISdoCollection> pClientsCollection;
   hr = vtClientsCollection.pdispVal->QueryInterface(      
      __uuidof(ISdoCollection), 
      (void **) &pClientsCollection
   );

   if (FAILED(hr))
   {
      return hr;
   }

```



## <a name="remarks"></a>Comentarios

La variable pSdoServiceControl contiene un puntero a un objeto de datos de servidor para NPS. Para obtener más información, vea el tema [Recuperación de un SDO de servicio.](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)

La variable vtClientsCollection es de tipo [ \_ variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)). Un objeto variant t encapsula o incluye \_ el tipo de datos \_ [**VARIANT.**](/windows/win32/api/oaidl/ns-oaidl-variant) La clase administra la asignación y desasignación de recursos, y realiza llamadas de función [**a VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) [**y VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) según corresponda.

Después de llamar a "pSdo->GetProperty()", la variable vtProtocolsCollection especifica un objeto . El **miembro pdispVal** de vtProtocolsCollection contiene un puntero a la [**interfaz IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) del objeto .

El código de ejemplo anterior se puede adaptar para recuperar otras colecciones nps, por ejemplo, las colecciones de controladores de solicitudes nps. El [**tipo de enumeración IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) enumeraba los valores que corresponden a las colecciones NPS disponibles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[\_variant \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))
</dt> <dt>

[**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> <dt>

[**ISdo::GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[Recuperar un SDO de servicio](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[**Variante**](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 