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
# <a name="retrieving-a-collection"></a><span data-ttu-id="c8af5-103">Recuperación de una colección</span><span class="sxs-lookup"><span data-stu-id="c8af5-103">Retrieving a Collection</span></span>

> [!Note]  
> <span data-ttu-id="c8af5-104">Se ha cambiado el nombre del servicio de autenticación de Internet (IAS) a partir de Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="c8af5-104">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="c8af5-105">El contenido de este tema se aplica a IAS y NPS.</span><span class="sxs-lookup"><span data-stu-id="c8af5-105">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="c8af5-106">En todo el texto, NPS se usa para hacer referencia a todas las versiones del servicio, incluidas las versiones mencionadas originalmente como IAS.</span><span class="sxs-lookup"><span data-stu-id="c8af5-106">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="c8af5-107">El código siguiente recupera la recopilación de clientes para el servidor de directivas de redes.</span><span class="sxs-lookup"><span data-stu-id="c8af5-107">The following code retrieves the clients collection for the Network Policy Server.</span></span>


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



## <a name="remarks"></a><span data-ttu-id="c8af5-108">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c8af5-108">Remarks</span></span>

<span data-ttu-id="c8af5-109">La variable pSdoServiceControl contiene un puntero a un objeto de datos de servidor para NPS.</span><span class="sxs-lookup"><span data-stu-id="c8af5-109">The pSdoServiceControl variable contains a pointer to a Server Data Object for NPS.</span></span> <span data-ttu-id="c8af5-110">Para obtener más información, vea el tema [recuperar un SDO de servicio](/windows/desktop/Nps/sdo-retrieving-a-service-sdo).</span><span class="sxs-lookup"><span data-stu-id="c8af5-110">For more information, see the topic [Retrieving a Service SDO](/windows/desktop/Nps/sdo-retrieving-a-service-sdo).</span></span>

<span data-ttu-id="c8af5-111">La variable vtClientsCollection es de tipo [ \_ variante \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)).</span><span class="sxs-lookup"><span data-stu-id="c8af5-111">The vtClientsCollection variable is of type [\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60)).</span></span> <span data-ttu-id="c8af5-112">Un \_ \_ objeto Variant t encapsula, o agrega, el tipo de datos [**Variant**](/windows/win32/api/oaidl/ns-oaidl-variant) .</span><span class="sxs-lookup"><span data-stu-id="c8af5-112">A \_variant\_t object encapsulates, or encloses, the [**VARIANT**](/windows/win32/api/oaidl/ns-oaidl-variant) data type.</span></span> <span data-ttu-id="c8af5-113">La clase administra la asignación y desasignación de recursos, y realiza llamadas de función a [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) y [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) según corresponda.</span><span class="sxs-lookup"><span data-stu-id="c8af5-113">The class manages resource allocation and deallocation, and makes function calls to [**VariantInit**](/windows/win32/api/oleauto/nf-oleauto-variantinit) and [**VariantClear**](/windows/win32/api/oleauto/nf-oleauto-variantclear) as appropriate.</span></span>

<span data-ttu-id="c8af5-114">Después de la llamada a "pSdo->GetProperty ()", la variable vtProtocolsCollection especifica un objeto.</span><span class="sxs-lookup"><span data-stu-id="c8af5-114">After the call to "pSdo->GetProperty()", the vtProtocolsCollection variable specifies an object.</span></span> <span data-ttu-id="c8af5-115">El miembro **pdispVal** de vtProtocolsCollection contiene un puntero a la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) para el objeto.</span><span class="sxs-lookup"><span data-stu-id="c8af5-115">The **pdispVal** member of vtProtocolsCollection contains a pointer to the [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) interface for the object.</span></span>

<span data-ttu-id="c8af5-116">El código de ejemplo anterior se puede adaptar para recuperar otras recopilaciones de NPS, por ejemplo, las colecciones de controladores de solicitud NPS.</span><span class="sxs-lookup"><span data-stu-id="c8af5-116">The above sample code can be adapted to retrieve other NPS collections, for example the NPS Request Handlers collections.</span></span> <span data-ttu-id="c8af5-117">El tipo de enumeración [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) enumera los valores que corresponden a las colecciones de NPS disponibles.</span><span class="sxs-lookup"><span data-stu-id="c8af5-117">The [**IASPROPERTIES**](/windows/desktop/api/sdoias/ne-sdoias-iasproperties) enumeration type enumerated values that correspond to the available NPS collections.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c8af5-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c8af5-118">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c8af5-119">[\_variante \_ t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span><span class="sxs-lookup"><span data-stu-id="c8af5-119">[\_variant\_t](/previous-versions/visualstudio/visual-studio-6.0/aa278648(v=vs.60))</span></span>
</dt> <dt>

[<span data-ttu-id="c8af5-120">**IASPROPERTIES**</span><span class="sxs-lookup"><span data-stu-id="c8af5-120">**IASPROPERTIES**</span></span>](/windows/desktop/api/sdoias/ne-sdoias-iasproperties)
</dt> <dt>

[<span data-ttu-id="c8af5-121">**ISdo:: GetProperty**</span><span class="sxs-lookup"><span data-stu-id="c8af5-121">**ISdo::GetProperty**</span></span>](/windows/desktop/api/sdoias/nf-sdoias-isdo-getproperty)
</dt> <dt>

[<span data-ttu-id="c8af5-122">**ISdoCollection**</span><span class="sxs-lookup"><span data-stu-id="c8af5-122">**ISdoCollection**</span></span>](/windows/desktop/api/sdoias/nn-sdoias-isdocollection)
</dt> <dt>

[<span data-ttu-id="c8af5-123">Recuperación de un SDO de servicio</span><span class="sxs-lookup"><span data-stu-id="c8af5-123">Retrieving a Service SDO</span></span>](/windows/desktop/Nps/sdo-retrieving-a-service-sdo)
</dt> <dt>

[<span data-ttu-id="c8af5-124">**VariantClear**</span><span class="sxs-lookup"><span data-stu-id="c8af5-124">**VariantClear**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantclear)
</dt> <dt>

[<span data-ttu-id="c8af5-125">**VariantInit**</span><span class="sxs-lookup"><span data-stu-id="c8af5-125">**VariantInit**</span></span>](/windows/win32/api/oleauto/nf-oleauto-variantinit)
</dt> <dt>

[<span data-ttu-id="c8af5-126">**VARIANTE**</span><span class="sxs-lookup"><span data-stu-id="c8af5-126">**VARIANT**</span></span>](/windows/win32/api/oaidl/ns-oaidl-variant)
</dt> </dl>

 

 