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
# <a name="writing-a-custom-surrogate"></a>Escritura de un suplente personalizado

Aunque el suplente proporcionado por el sistema será más adecuado para la mayoría de los casos, hay algunos casos en los que la escritura de un suplente personalizado podría merecer la pena. A continuación se muestran algunos ejemplos:

-   Un suplente personalizado podría proporcionar algunas optimizaciones o semánticas que no están presentes en el suplente del sistema.
-   Si una DLL en proceso contiene código que depende de estar en el mismo proceso que el cliente, el servidor DLL no funcionará correctamente si se ejecuta en el suplente del sistema. Un suplente personalizado se puede adaptar a un archivo DLL específico para solucionar este error.
-   El suplente del sistema admite un modelo de subprocesamiento mixto para que pueda cargar los archivos DLL del modelo de apartamento y de forma libre. Un suplente personalizado se puede adaptar para cargar solo los archivos dll de apartamento por motivos de eficacia o para aceptar un argumento de línea de comandos para el tipo de archivo DLL que se puede cargar.
-   Un suplente personalizado podría tomar parámetros de línea de comandos adicionales que el suplente del sistema no.
-   El suplente del sistema llama a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) e indica a que use cualquier configuración de seguridad existente que se encuentre en la clave [AppID](appid-key.md) del registro. Un suplente personalizado podría usar otro contexto de seguridad.
-   Las interfaces que no son remotas (por ejemplo, las de ocx recientes) no funcionarán con el suplente del sistema. Un suplente personalizado podría encapsular las interfaces del archivo DLL con su propia implementación y usar archivos dll de proxy/código auxiliar con una definición de IDL remoto que permitiera que la interfaz fuera remota.

Normalmente, el subproceso suplente principal debe realizar los siguientes pasos de configuración:

1.  Llame a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar el subproceso y establecer el modelo de subprocesos.
2.  Si desea que los servidores DLL que se ejecutan en el servidor puedan usar la configuración de seguridad en la clave del registro **AppID** , llame a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) con la funcionalidad de EOAC \_ AppID. De lo contrario, se usará la configuración de seguridad heredada.
3.  Llame a [**CoRegisterSurrogate**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) para registrar la interfaz suplente en com.
4.  Llame a [**ISurrogate:: LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) para el CLSID solicitado.
5.  Coloque el subproceso principal en un bucle para llamar a [**CoFreeUnusedLibraries**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries) periódicamente.
6.  Cuando COM llama a [**ISurrogate:: FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), revoca todos los generadores de clases y sale.

Un proceso suplente debe implementar la interfaz [**ISurrogate**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) . Esta interfaz se debe registrar cuando se inicia un nuevo suplente y después de llamar a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). Como se indicó en los pasos anteriores, la interfaz **ISurrogate** tiene dos métodos que com llama: [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), para cargar dinámicamente nuevos servidores dll en suplentes existentes. y [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), para liberar el suplente.

La implementación de [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), que llama a com con una solicitud de carga, debe crear primero un objeto de generador de clases que admita [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown), [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)y [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)y, a continuación, llamar a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) para registrar el objeto como el generador de clases para el CLSID solicitado.

El generador de clases registrado por el proceso suplente no es el generador de clases real implementado por el servidor DLL, pero es un generador de clases genérico implementado por el proceso suplente que admite [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) e [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal). Dado que es el generador de clases del suplente, en lugar del servidor DLL que se está registrando, el generador de clases del suplente tendrá que usar el generador de clases real para crear una instancia del objeto para el CLSID registrado. [**IClassFactory:: CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) del suplente debe ser similar al ejemplo siguiente:


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



El generador de clases del suplente también debe admitir [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) porque una llamada a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) puede solicitar cualquier interfaz del generador de clases registrado, no solo [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory). Además, dado que el generador de clases genérico solo admite [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) y **IClassFactory**, las solicitudes de otras interfaces deben dirigirse al objeto real. Por lo tanto, debería haber un método [**MarshalInterface (**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) que debería ser similar al siguiente:


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



El suplente que aloja un servidor DLL debe publicar los objetos de clase del servidor DLL con una llamada a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject). Todos los generadores de clases para los suplentes de DLL deben registrarse como \_ suplente REGCLS. REGCLS \_ SINGLUSE y REGCLS \_ MULTIPLEUSE no deben usarse para los servidores dll cargados en suplentes.

Si se siguen estas directrices para crear un proceso suplente cuando sea necesario hacerlo, se debe garantizar el comportamiento correcto.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suplentes DLL](dll-surrogates.md)
</dt> </dl>

 

 