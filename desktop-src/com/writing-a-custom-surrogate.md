---
title: Escritura de un suplente personalizado
description: Escritura de un suplente personalizado
ms.assetid: 510e38e5-1965-46f4-b09c-6fa585cff993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0899702f6626d586f8a819e8fee2c2e67b7c80
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104359433"
---
# <a name="writing-a-custom-surrogate"></a><span data-ttu-id="14488-103">Escritura de un suplente personalizado</span><span class="sxs-lookup"><span data-stu-id="14488-103">Writing a Custom Surrogate</span></span>

<span data-ttu-id="14488-104">Aunque el suplente proporcionado por el sistema será más adecuado para la mayoría de los casos, hay algunos casos en los que la escritura de un suplente personalizado podría merecer la pena.</span><span class="sxs-lookup"><span data-stu-id="14488-104">While the system-supplied surrogate will be more than adequate for most situations, there are some cases where writing a custom surrogate could be worthwhile.</span></span> <span data-ttu-id="14488-105">A continuación se muestran algunos ejemplos:</span><span class="sxs-lookup"><span data-stu-id="14488-105">Following are some examples:</span></span>

-   <span data-ttu-id="14488-106">Un suplente personalizado podría proporcionar algunas optimizaciones o semánticas que no están presentes en el suplente del sistema.</span><span class="sxs-lookup"><span data-stu-id="14488-106">A custom surrogate could provide some optimizations or semantics not present in the system surrogate.</span></span>
-   <span data-ttu-id="14488-107">Si una DLL en proceso contiene código que depende de estar en el mismo proceso que el cliente, el servidor DLL no funcionará correctamente si se ejecuta en el suplente del sistema.</span><span class="sxs-lookup"><span data-stu-id="14488-107">If an in-process DLL contains code that depends on being in the same process as the client, the DLL server will not function correctly if it is running in the system surrogate.</span></span> <span data-ttu-id="14488-108">Un suplente personalizado se puede adaptar a un archivo DLL específico para solucionar este error.</span><span class="sxs-lookup"><span data-stu-id="14488-108">A custom surrogate could be tailored to a specific DLL to deal with this.</span></span>
-   <span data-ttu-id="14488-109">El suplente del sistema admite un modelo de subprocesamiento mixto para que pueda cargar los archivos DLL del modelo de apartamento y de forma libre.</span><span class="sxs-lookup"><span data-stu-id="14488-109">The system surrogate supports a mixed-threading model so that it can load both free and apartment model DLLs.</span></span> <span data-ttu-id="14488-110">Un suplente personalizado se puede adaptar para cargar solo los archivos dll de apartamento por motivos de eficacia o para aceptar un argumento de línea de comandos para el tipo de archivo DLL que se puede cargar.</span><span class="sxs-lookup"><span data-stu-id="14488-110">A custom surrogate might be tailored to load only apartment DLLs for reasons of efficiency or to accept a command-line argument for the type of DLL it is allowed to load.</span></span>
-   <span data-ttu-id="14488-111">Un suplente personalizado podría tomar parámetros de línea de comandos adicionales que el suplente del sistema no.</span><span class="sxs-lookup"><span data-stu-id="14488-111">A custom surrogate could take extra command-line parameters that the system surrogate does not.</span></span>
-   <span data-ttu-id="14488-112">El suplente del sistema llama a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e indica a que use cualquier configuración de seguridad existente que se encuentre en la clave [AppID](appid-key.md) del registro.</span><span class="sxs-lookup"><span data-stu-id="14488-112">The system surrogate calls [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) and tells it to use any existing security settings found under the [AppID](appid-key.md) key in the registry.</span></span> <span data-ttu-id="14488-113">Un suplente personalizado podría usar otro contexto de seguridad.</span><span class="sxs-lookup"><span data-stu-id="14488-113">A custom surrogate could use another security context.</span></span>
-   <span data-ttu-id="14488-114">Las interfaces que no son remotas (por ejemplo, las de ocx recientes) no funcionarán con el suplente del sistema.</span><span class="sxs-lookup"><span data-stu-id="14488-114">Interfaces that aren't remotable (such as those for recent OCXs) will not work with the system surrogate.</span></span> <span data-ttu-id="14488-115">Un suplente personalizado podría encapsular las interfaces del archivo DLL con su propia implementación y usar archivos dll de proxy/código auxiliar con una definición de IDL remoto que permitiera que la interfaz fuera remota.</span><span class="sxs-lookup"><span data-stu-id="14488-115">A custom surrogate could wrap the DLL's interfaces with its own implementation and use proxy/stub DLLs with a remotable IDL definition that would allow the interface to be remoted.</span></span>

<span data-ttu-id="14488-116">Normalmente, el subproceso suplente principal debe realizar los siguientes pasos de configuración:</span><span class="sxs-lookup"><span data-stu-id="14488-116">The main surrogate thread should typically perform the following setup steps:</span></span>

1.  <span data-ttu-id="14488-117">Llame a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar el subproceso y establecer el modelo de subprocesos.</span><span class="sxs-lookup"><span data-stu-id="14488-117">Call [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) to initialize the thread and set the threading model.</span></span>
2.  <span data-ttu-id="14488-118">Si desea que los servidores DLL que se ejecutan en el servidor puedan usar la configuración de seguridad en la clave del registro **AppID** , llame a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) con la funcionalidad de EOAC \_ AppID.</span><span class="sxs-lookup"><span data-stu-id="14488-118">If you want the DLL servers that are to run in the server to be able to use the security settings in the **AppID** registry key, call [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) with the EOAC\_APPID capability.</span></span> <span data-ttu-id="14488-119">De lo contrario, se usará la configuración de seguridad heredada.</span><span class="sxs-lookup"><span data-stu-id="14488-119">Otherwise, legacy security settings will be used.</span></span>
3.  <span data-ttu-id="14488-120">Llame a [**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) para registrar la interfaz suplente en com.</span><span class="sxs-lookup"><span data-stu-id="14488-120">Call [**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) to register the surrogate interface to COM.</span></span>
4.  <span data-ttu-id="14488-121">Llame a [**ISurrogate:: LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) para el CLSID solicitado.</span><span class="sxs-lookup"><span data-stu-id="14488-121">Call [**ISurrogate::LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) for the requested CLSID.</span></span>
5.  <span data-ttu-id="14488-122">Coloque el subproceso principal en un bucle para llamar a [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) periódicamente.</span><span class="sxs-lookup"><span data-stu-id="14488-122">Put main thread in a loop to call [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) periodically.</span></span>
6.  <span data-ttu-id="14488-123">Cuando COM llama a [**ISurrogate:: FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), revoca todos los generadores de clases y sale.</span><span class="sxs-lookup"><span data-stu-id="14488-123">When COM calls [**ISurrogate::FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), revoke all class factories and exit.</span></span>

<span data-ttu-id="14488-124">Un proceso suplente debe implementar la interfaz [**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) .</span><span class="sxs-lookup"><span data-stu-id="14488-124">A surrogate process must implement the [**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) interface.</span></span> <span data-ttu-id="14488-125">Esta interfaz se debe registrar cuando se inicia un nuevo suplente y después de llamar a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span><span class="sxs-lookup"><span data-stu-id="14488-125">This interface should be registered when a new surrogate is started and after calling [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex).</span></span> <span data-ttu-id="14488-126">Como se indicó en los pasos anteriores, la interfaz **ISurrogate** tiene dos métodos que com llama: [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), para cargar dinámicamente nuevos servidores dll en suplentes existentes. y [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), para liberar el suplente.</span><span class="sxs-lookup"><span data-stu-id="14488-126">As indicated in the preceding steps, the **ISurrogate** interface has two methods that COM calls: [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), to dynamically load new DLL servers into existing surrogates; and [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), to free the surrogate.</span></span>

<span data-ttu-id="14488-127">La implementación de [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), que llama a com con una solicitud de carga, debe crear primero un objeto de generador de clases que admita [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)y [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)y, a continuación, llamar a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) para registrar el objeto como el generador de clases para el CLSID solicitado.</span><span class="sxs-lookup"><span data-stu-id="14488-127">The implementation of [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), which COM calls with a load request, must first create a class factory object that supports [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), and [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal), and then call [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) to register the object as the class factory for the requested CLSID.</span></span>

<span data-ttu-id="14488-128">El generador de clases registrado por el proceso suplente no es el generador de clases real implementado por el servidor DLL, pero es un generador de clases genérico implementado por el proceso suplente que admite [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) e [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal).</span><span class="sxs-lookup"><span data-stu-id="14488-128">The class factory registered by the surrogate process is not the actual class factory implemented by the DLL server but is a generic class factory implemented by the surrogate process that supports [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) and [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal).</span></span> <span data-ttu-id="14488-129">Dado que es el generador de clases del suplente, en lugar del servidor DLL que se está registrando, el generador de clases del suplente tendrá que usar el generador de clases real para crear una instancia del objeto para el CLSID registrado.</span><span class="sxs-lookup"><span data-stu-id="14488-129">Because it is the surrogate's class factory, rather than that of the DLL server that is being registered, the surrogate's class factory will need to use the real class factory to create an instance of the object for the registered CLSID.</span></span> <span data-ttu-id="14488-130">[**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) del suplente debe ser similar al ejemplo siguiente:</span><span class="sxs-lookup"><span data-stu-id="14488-130">The surrogate's [**IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) should look something like the following example:</span></span>


```C++
STDMETHODIMP CSurrogateFactory::CreateInstance(
  IUnknown* pUnkOuter, 
  REFIID iid, 
  void** ppv)
{
    void* pcf;
    HRESULT hr;
 
    hr = CoGetClassObject(clsid, CLSCTX_INPROC_SERVER, NULL, IID_IClassFactory, &pcf);
    if ( FAILED(hr) )
        return hr;
    hr = ((IClassFactory*)pcf)->CreateInstance(pUnkOuter, iid, ppv);
    ((IClassFactory*)pcf)->Release();
    return hr;
}
 
```



<span data-ttu-id="14488-131">El generador de clases del suplente también debe admitir [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) porque una llamada a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) puede solicitar cualquier interfaz del generador de clases registrado, no solo [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span><span class="sxs-lookup"><span data-stu-id="14488-131">The surrogate's class factory must also support [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) because a call to [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) can request any interface from the registered class factory, not just [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory).</span></span> <span data-ttu-id="14488-132">Además, dado que el generador de clases genérico solo admite [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) y **IClassFactory**, las solicitudes de otras interfaces deben dirigirse al objeto real.</span><span class="sxs-lookup"><span data-stu-id="14488-132">Further, since the generic class factory supports only [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) and **IClassFactory**, requests for other interfaces must be directed to the real object.</span></span> <span data-ttu-id="14488-133">Por lo tanto, debería haber un método [**MarshalInterface (**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) que debería ser similar al siguiente:</span><span class="sxs-lookup"><span data-stu-id="14488-133">Thus, there should be a [**MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) method which should be similar to the following:</span></span>


```C++
STDMETHODIMP CSurrogateFactory::MarshalInterface(
  IStream *pStm,  
  REFIID riid, void *pv, 
  WORD dwDestContext, 
  void *pvDestContext, 
  DWORD mshlflags )
{   
    void * pCF = NULL;
    HRESULT hr;
 
    hr = CoGetClassObject(clsid, CLSCTX_INPROC_SERVER, NULL, riid, &pCF);
    if ( FAILED(hr) )
        return hr;   
    hr = CoMarshalInterface(pStm, riid, (IUnknown*)pCF, dwDestContext, pvDestContext,  mshlflags);
    ((IUnknown*)pCF)->Release();
    return S_OK;
 
```



<span data-ttu-id="14488-134">El suplente que aloja un servidor DLL debe publicar los objetos de clase del servidor DLL con una llamada a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject).</span><span class="sxs-lookup"><span data-stu-id="14488-134">The surrogate that houses a DLL server must publish the DLL server's class object(s) with a call to [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject).</span></span> <span data-ttu-id="14488-135">Todos los generadores de clases para los suplentes de DLL deben registrarse como \_ suplente REGCLS.</span><span class="sxs-lookup"><span data-stu-id="14488-135">All class factories for DLL surrogates should be registered as REGCLS\_SURROGATE.</span></span> <span data-ttu-id="14488-136">REGCLS \_ SINGLUSE y REGCLS \_ MULTIPLEUSE no deben usarse para los servidores dll cargados en suplentes.</span><span class="sxs-lookup"><span data-stu-id="14488-136">REGCLS\_SINGLUSE and REGCLS\_MULTIPLEUSE should not be used for DLL servers loaded into surrogates.</span></span>

<span data-ttu-id="14488-137">Si se siguen estas directrices para crear un proceso suplente cuando sea necesario hacerlo, se debe garantizar el comportamiento correcto.</span><span class="sxs-lookup"><span data-stu-id="14488-137">Following these guidelines for creating a surrogate process when it is necessary to do so should ensure proper behavior.</span></span>

## <a name="related-topics"></a><span data-ttu-id="14488-138">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="14488-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="14488-139">Suplentes DLL</span><span class="sxs-lookup"><span data-stu-id="14488-139">DLL Surrogates</span></span>](dll-surrogates.md)
</dt> </dl>

 

 