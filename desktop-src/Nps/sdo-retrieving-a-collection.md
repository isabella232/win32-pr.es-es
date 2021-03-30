---
title: Recuperación de una colección
description: Recuperación de una colección
ms.assetid: b9090ad5-564c-4f48-b7bd-24617d582d2e
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 517acfa320069f9c94ee291e9215459d27ba25ad
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "103995435"
---
# <a name="retrieving-a-collection"></a>Recuperación de una colección

> [!Note]  
> Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008. El contenido de este tema se aplica a IAS y NPS. En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.

 

El código siguiente recupera la recopilación de clientes para el servidor de directivas de redes.


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



## <a name="remarks"></a>Observaciones

La variable pSdoServiceControl contiene un puntero a un objeto de datos de servidor para NPS. Para obtener más información, vea el tema [recuperar un SDO de servicio](/windows/desktop/Nps/sdo-retrieving-a-service-sdo).

La variable vtClientsCollection es de tipo [ \_ variante \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)). Un \_ \_ objeto Variant t encapsula, o agrega, el tipo de datos [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) . La clase administra la asignación y desasignación de recursos, y realiza llamadas de función a [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) y [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) según corresponda.

Después de la llamada a "pSdo->GetProperty ()", la variable vtProtocolsCollection especifica un objeto. El miembro **pdispVal** de vtProtocolsCollection contiene un puntero a la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) para el objeto.

El código de ejemplo anterior se puede adaptar para recuperar otras recopilaciones de NPS, por ejemplo, las colecciones de controladores de solicitud NPS. El tipo de enumeración [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) enumera los valores que corresponden a las colecciones de NPS disponibles.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[\_variante \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))
</dt> <dt>

[**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> <dt>

[**ISdo:: GetProperty**](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[**ISdoCollection**](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[Recuperación de un SDO de servicio](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[**VARIANTE**](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 