---
title: Configuración de la interfaz de usuario del método EAP
description: Explica cómo configurar el suplicante proporcionando una configuración de método EAP a EAPHost.
ms.assetid: f6a23201-e221-4098-863f-71a81735d927
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9b82debadc075b1fcc12dad06484c0fd3617874
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/26/2019
ms.locfileid: "105714317"
---
# <a name="configuring-the-eap-method-user-interface"></a><span data-ttu-id="9dce6-103">Configuración de la interfaz de usuario del método EAP</span><span class="sxs-lookup"><span data-stu-id="9dce6-103">Configuring the EAP Method User Interface</span></span>

<span data-ttu-id="9dce6-104">En este tema se explica cómo configurar el suplicante proporcionando una configuración de método EAP a EAPHost.</span><span class="sxs-lookup"><span data-stu-id="9dce6-104">This topic explains how to configure the supplicant by supplying an EAP method configuration to EAPHost.</span></span>

<span data-ttu-id="9dce6-105">Para que un solicitante realice una autenticación basada en EAP mediante EAPHost, un suplicante debe proporcionar una configuración de método EAP a EAPHost a través de la función [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) .</span><span class="sxs-lookup"><span data-stu-id="9dce6-105">For a supplicant to perform an EAP-based authentication using EAPHost, a supplicant must supply an EAP method configuration to EAPHost through the [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) function.</span></span>

1.  <span data-ttu-id="9dce6-106">Para obtener la configuración del método EAP, un suplicante normalmente consulta a EAPHost mediante [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) para obtener información sobre el conjunto completo de métodos EAP que están disponibles e instalados en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="9dce6-106">To obtain the EAP method configuration, a supplicant typically queries EAPHost using [**EapHostPeerGetMethods**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeergetmethods) to learn the complete set of EAP methods that are available and installed on the local machine.</span></span> <span data-ttu-id="9dce6-107">La lista de métodos normalmente se presenta al usuario en un cuadro combinado u otro control de la interfaz de usuario que permite al usuario seleccionar el método que deseen.</span><span class="sxs-lookup"><span data-stu-id="9dce6-107">The list of methods is typically presented to the user in a combination box or other UI control that allows the user to select the method they want.</span></span>
    > [!Note]  
    > <span data-ttu-id="9dce6-108">El suplicante puede elegir filtrar la lista de métodos mostrada en función de los bits de propiedad de método indicados en el **método de EAP \_ \_ info. eapProperties**.</span><span class="sxs-lookup"><span data-stu-id="9dce6-108">The supplicant may choose to filter the displayed list of methods based on the method property bits indicated in **EAP\_METHOD\_INFO.eapProperties**.</span></span> <span data-ttu-id="9dce6-109">Algunos métodos pueden no ser adecuados para las características de seguridad del transporte proporcionado por el suplicante, por ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9dce6-109">Some methods may not be appropriate for the security characteristics of the transport provided by the supplicant, for example.</span></span>

     

2.  <span data-ttu-id="9dce6-110">Una vez que el control de IU se rellena con el conjunto de posibles métodos EAP, el usuario selecciona el método que desea configurar.</span><span class="sxs-lookup"><span data-stu-id="9dce6-110">Once the UI control is populated with the set of possible EAP methods, the user selects the method they want to configure.</span></span> <span data-ttu-id="9dce6-111">Normalmente, el solicitante proporciona un botón de **configuración** o de **propiedades** para que el usuario tenga acceso a las propiedades de configuración del método EAP seleccionado.</span><span class="sxs-lookup"><span data-stu-id="9dce6-111">Typically, the supplicant provides a **Configuration** or **Properties** button for the user to access configuration properties of the selected EAP method.</span></span>
    > [!Note]
    > <span data-ttu-id="9dce6-112">El suplicante es consciente de que hay propiedades configurables por el usuario basadas en el bit **eapPropSupportsConfig** que se está habilitando en la **información del \_ método EAP \_ . eapProperties**.</span><span class="sxs-lookup"><span data-stu-id="9dce6-112">The supplicant is aware that there are user-configurable properties based on the **eapPropSupportsConfig** bit being enabled in **EAP\_METHOD\_INFO.eapProperties**.</span></span>
    >
    > <span data-ttu-id="9dce6-113">Para obtener más información, vea [**propiedades del método EAP**](eap-method-properties.md).</span><span class="sxs-lookup"><span data-stu-id="9dce6-113">For more information, see [**EAP Method Properties**](eap-method-properties.md).</span></span>

     

3.  <span data-ttu-id="9dce6-114">Cuando el usuario hace clic en el control de IU adecuado, el solicitante llama a [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), pasando la función el valor **hWnd** para la interfaz de usuario propia del suplicante, la estructura de [**\_ \_ tipo del método EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) obtenida de la consulta a la estructura de [**\_ \_ información del método EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) y otros parámetros necesarios.</span><span class="sxs-lookup"><span data-stu-id="9dce6-114">When the user clicks the appropriate UI control, the supplicant calls [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui), passing into the function the **HWND** value for the supplicant's own UI, the [**EAP\_METHOD\_TYPE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) structure obtained from the query to [**EAP\_METHOD\_INFO**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_info) structure and other required parameters.</span></span>
4.  <span data-ttu-id="9dce6-115">La llamada a [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) invoca la interfaz de usuario de configuración de un método EAP.</span><span class="sxs-lookup"><span data-stu-id="9dce6-115">Calling [**EapHostPeerInvokeConfigUI**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerinvokeconfigui) invokes an EAP method's own configuration UI.</span></span> <span data-ttu-id="9dce6-116">En la devolución de **EapHostPeerInvokeConfigUI**, la función devolverá un BLOB de configuración del método EAP como parámetro out.</span><span class="sxs-lookup"><span data-stu-id="9dce6-116">On return from **EapHostPeerInvokeConfigUI**, the function will return an EAP method configuration BLOB as an out-parameter.</span></span>
5.  <span data-ttu-id="9dce6-117">El suplicante almacena el BLOB de configuración, junto con la estructura de [**\_ \_ tipo de método EAP**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) para su uso con [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span><span class="sxs-lookup"><span data-stu-id="9dce6-117">The supplicant stores the configuration BLOB, along with the [**EAP\_METHOD\_TYPE**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_method_type) structure for use with [**EapHostPeerBeginSession**](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession).</span></span>
6.  <span data-ttu-id="9dce6-118">El método preciso para almacenar el BLOB configuración es totalmente el solicitante.</span><span class="sxs-lookup"><span data-stu-id="9dce6-118">The precise method for storing the configuraiton BLOB is entirely up to the supplicant.</span></span> <span data-ttu-id="9dce6-119">Sin embargo, el suplicante siempre debe almacenar la configuración de forma adecuada y segura adecuada para los datos de configuración de autenticación del sistema y del usuario.</span><span class="sxs-lookup"><span data-stu-id="9dce6-119">However, the supplicant should always store the configuration in a suitable, secure manner appropriate for system and user authentication configuration data.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9dce6-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9dce6-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dce6-121">Habilitar directiva de grupo</span><span class="sxs-lookup"><span data-stu-id="9dce6-121">Enabling Group Policy</span></span>](enabling-group-policy.md)
</dt> <dt>

[<span data-ttu-id="9dce6-122">Implementación de la compatibilidad de In-Band NAP con métodos EAP</span><span class="sxs-lookup"><span data-stu-id="9dce6-122">Implementing In-Band NAP Support for EAP Methods</span></span>](enabling-in-band-nap-support.md)
</dt> <dt>

[<span data-ttu-id="9dce6-123">Implementación de la compatibilidad de NAP con métodos EAP</span><span class="sxs-lookup"><span data-stu-id="9dce6-123">Implementing NAP Support for EAP Methods</span></span>](implementing-nap-for-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="9dce6-124">Transferencia de datos entre el suplicante y los métodos EAP</span><span class="sxs-lookup"><span data-stu-id="9dce6-124">Transferring Data Between the Supplicant and EAP Methods</span></span>](transferring-data-between-the-supplicant-and-eap-methods.md)
</dt> <dt>

[<span data-ttu-id="9dce6-125">Suplicantes de EAPHost</span><span class="sxs-lookup"><span data-stu-id="9dce6-125">EAPHost Supplicants</span></span>](eaphost-supplicants.md)
</dt> </dl>

 

 




