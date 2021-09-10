---
title: Escritura de un suplente personalizado
description: Escritura de un suplente personalizado
ms.assetid: 510e38e5-1965-46f4-b09c-6fa585cff993
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af0899702f6626d586f8a819e8fee2c2e67b7c80
ms.sourcegitcommit: 9eebab0ead09cecdbc24f5f84d56c8b6a7c22736
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/10/2021
ms.locfileid: "124369720"
---
# <a name="writing-a-custom-surrogate"></a>Escritura de un suplente personalizado

Aunque el suplente proporcionado por el sistema será más que adecuado para la mayoría de las situaciones, hay algunos casos en los que podría merecer la pena escribir un suplente personalizado. A continuación se muestran algunos ejemplos:

-   Un suplente personalizado podría proporcionar algunas optimizaciones o semánticas que no están presentes en el suplente del sistema.
-   Si un archivo DLL en proceso contiene código que depende de estar en el mismo proceso que el cliente, el servidor DLL no funcionará correctamente si se ejecuta en el suplente del sistema. Un suplente personalizado podría adaptarse a un archivo DLL específico para tratar con esto.
-   El suplente del sistema admite un modelo de subprocesos mixtos para que pueda cargar archivos DLL de modelo de apartamento y gratis. Un suplente personalizado podría adaptarse para cargar solo archivos DLL de apartamento por motivos de eficacia o para aceptar un argumento de línea de comandos para el tipo de ARCHIVO DLL que se puede cargar.
-   Un suplente personalizado podría tomar parámetros de línea de comandos adicionales que el suplente del sistema no hace.
-   El suplente del sistema llama a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) y le indica que use cualquier configuración de seguridad existente que se encuentra en la clave [AppID](appid-key.md) del Registro. Un suplente personalizado podría usar otro contexto de seguridad.
-   Las interfaces que no son remotables (como las de los OCX recientes) no funcionarán con el suplente del sistema. Un suplente personalizado podría encapsular las interfaces del archivo DLL con su propia implementación y usar archivos DLL de proxy o de código auxiliar con una definición de IDL remota que permitiría el control remoto de la interfaz.

Normalmente, el subproceso suplente principal debe realizar los siguientes pasos de configuración:

1.  Llame [**a CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex) para inicializar el subproceso y establecer el modelo de subprocesos.
2.  Si desea que los servidores DLL que se van a ejecutar en el servidor puedan usar la configuración de seguridad en la clave del Registro **AppID,** llame a [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) con la funcionalidad APPID de \_ EOAC. De lo contrario, se usará la configuración de seguridad heredada.
3.  Llame [**a CoRegisterSurrogate para**](/windows/desktop/api/combaseapi/nf-combaseapi-coregistersurrogate) registrar la interfaz suplente en COM.
4.  Llame [**a ISurrogate::LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver) para el CLSID solicitado.
5.  Coloque el subproceso principal en un bucle para llamar periódicamente a [**CoFreeUnusedLibraries.**](/windows/desktop/api/combaseapi/nf-combaseapi-cofreeunusedlibraries)
6.  Cuando COM llama [**a ISurrogate::FreeSurrogate,**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate)revoque todos los generadores de clases y salga.

Un proceso suplente debe implementar la [**interfaz ISurrogate.**](/windows/win32/api/objidlbase/nn-objidlbase-isurrogate) Esta interfaz se debe registrar cuando se inicia un nuevo suplente y después de llamar a [**CoInitializeEx**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializeex). Como se indica en los pasos anteriores, la interfaz **ISurrogate** tiene dos métodos a los que llama COM: [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), para cargar dinámicamente nuevos servidores DLL en suplentes existentes. y [**FreeSurrogate**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-freesurrogate), para liberar el suplente.

La implementación de [**LoadDllServer**](/windows/win32/api/objidlbase/nf-objidlbase-isurrogate-loaddllserver), que llama a COM con una solicitud de carga, debe crear primero un objeto de generador de clases que admita [**IUnknown,**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory)e [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal)y, a continuación, llamar a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject) para registrar el objeto como generador de clases para el CLSID solicitado.

El generador de clases registrado por el proceso suplente no es el generador de clases real implementado por el servidor DLL, pero es un generador de clases genérico implementado por el proceso suplente que admite [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) e [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal). Dado que es el generador de clases del suplente, en lugar del del servidor DLL que se está registrando, el generador de clases del suplente deberá usar el generador de clases reales para crear una instancia del objeto para el CLSID registrado. El elemento [**IClassFactory::CreateInstance**](/windows/desktop/api/Unknwn/nf-unknwn-iclassfactory-createinstance) del suplente debe tener un aspecto parecido al del ejemplo siguiente:


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



El generador de clases del suplente también debe admitir [**IMarshal**](/windows/win32/api/objidlbase/nn-objidlbase-imarshal) porque una llamada a [**CoGetClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-cogetclassobject) puede solicitar cualquier interfaz del generador de clases registrado, no solo [**IClassFactory.**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory) Además, dado que el generador de clases genéricas solo admite [**IUnknown**](/windows/desktop/api/Unknwn/nn-unknwn-iunknown) e **IClassFactory,** las solicitudes de otras interfaces deben dirigirse al objeto real. Por lo tanto, debe haber un [**método MarshalInterface**](/windows/win32/api/objidlbase/nf-objidlbase-imarshal-marshalinterface) similar al siguiente:


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



El suplente que aloja un servidor DLL debe publicar los objetos de clase del servidor DLL con una llamada a [**CoRegisterClassObject**](/windows/desktop/api/combaseapi/nf-combaseapi-coregisterclassobject). Todos los generadores de clases para suplentes dll deben registrarse como REGCLS \_ SURROGATE. REGCLS SINGLUSE y REGCLS MULTIPLEUSE no deben usarse para servidores \_ \_ DLL cargados en suplentes.

Seguir estas directrices para crear un proceso suplente cuando sea necesario hacerlo debe garantizar un comportamiento adecuado.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Suplentes de DLL](dll-surrogates.md)
</dt> </dl>

 

 