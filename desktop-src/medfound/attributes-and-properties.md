---
description: Un atributo es un par clave-valor, donde la clave es un GUID y el valor es PROPVARIANT. Los atributos se usan en Microsoft Media Foundation para configurar objetos, describir formatos multimedia, propiedades de objetos de consulta y otros propósitos.
ms.assetid: 44af5e03-5f0a-4564-b9d6-b8c935df35b2
title: Atributos en Media Foundation
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f46cc919f426ff7b0862de73d8852291d25b7e31f2b5d67d7a4955369be6d17
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943305"
---
# <a name="attributes-in-media-foundation"></a>Atributos en Media Foundation

Un atributo es un par clave-valor, donde la clave es un GUID y el valor **es PROPVARIANT.** Los atributos se usan en Microsoft Media Foundation para configurar objetos, describir formatos multimedia, propiedades de objetos de consulta y otros propósitos.

En este tema se incluyen las siguientes secciones.

-   [Acerca de atributos](#about-attributes)
-   [Serialización de atributos](#serializing-attributes)
-   [Implementación deATTRIBUTEAttributes](#implementing-imfattributes)
-   [Temas relacionados](#related-topics)

## <a name="about-attributes"></a>Acerca de atributos

Un atributo es un par clave-valor, donde la clave es un GUID y el valor **es PROPVARIANT.** Los valores de atributo están restringidos a los siguientes tipos de datos:

-   Entero de 32 bits sin signo (**UINT32**).
-   Entero de 64 bits sin signo (**UINT64**).
-   Número de punto flotante de 64 bits.
-   GUID.
-   Cadena de caracteres anchos terminada en NULL.
-   Matriz de bytes.
-   **Puntero IUnknown.**

Estos tipos se definen en la [**enumeración MF \_ ATTRIBUTE \_ TYPE.**](/windows/desktop/api/mfobjects/ne-mfobjects-mf_attribute_type) Para establecer o recuperar valores de atributo, use la [**interfaz IMFAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Esta interfaz contiene métodos con seguridad de tipos para obtener y establecer valores por tipo de datos. Por ejemplo, para establecer un entero de 32 bits, llame [**aATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32). Las claves de atributo son únicas dentro de un objeto . Si establece dos valores diferentes con la misma clave, el segundo valor sobrescribe el primero.

Varias Media Foundation interfaz heredan [**la interfaz DEATTRIBUTEAttributes.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) Los objetos que exponen esta interfaz tienen atributos opcionales o obligatorios que la aplicación debe establecer en el objeto o tienen atributos que la aplicación puede recuperar. Además, algunos métodos y funciones toman **un puntero IMFAttributes** como parámetro, lo que permite a la aplicación establecer información de configuración. La aplicación debe crear un almacén de atributos para contener los atributos de configuración. Para crear un almacén de atributos vacío, llame [**a MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes).

En el código siguiente se muestran dos funciones. El primero crea un nuevo almacén de atributos y establece un atributo hipotético denominado MY \_ ATTRIBUTE con un valor de cadena. La segunda función recupera el valor de este atributo.


```C++
extern const GUID MY_ATTRIBUTE;

HRESULT ShowCreateAttributeStore(IMFAttributes **ppAttributes)
{
    IMFAttributes *pAttributes = NULL;
    const UINT32 cElements = 10;  // Starting size.

    // Create the empty attribute store.
    HRESULT hr = MFCreateAttributes(&pAttributes, cElements);

    // Set the MY_ATTRIBUTE attribute with a string value.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetString(
            MY_ATTRIBUTE,
            L"This is a string value"
            );
    }

    // Return the IMFAttributes pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppAttributes = pAttributes;
        (*ppAttributes)->AddRef();
    }

    SAFE_RELEASE(pAttributes);

    return hr;
}

HRESULT ShowGetAttributes()
{
    IMFAttributes *pAttributes = NULL;
    WCHAR *pwszValue = NULL;
    UINT32 cchLength = 0;

    // Create the attribute store.
    HRESULT hr = ShowCreateAttributeStore(&pAttributes);

    // Get the attribute.
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->GetAllocatedString(
            MY_ATTRIBUTE,
            &pwszValue,
            &cchLength
            );
    }

    CoTaskMemFree(pwszValue);
    SAFE_RELEASE(pAttributes);

    return hr;
}
```



Para obtener una lista completa de Media Foundation atributos, [vea Media Foundation Atributos .](media-foundation-attributes.md) El tipo de datos esperado para cada atributo se documenta allí.

## <a name="serializing-attributes"></a>Serialización de atributos

Media Foundation tiene dos funciones para serializar almacenes de atributos. Uno escribe los atributos en una matriz de bytes y el otro los escribe en una secuencia que admite la **interfaz IStream.** Cada función tiene una función correspondiente que carga los datos.



| Operación | Matriz de bytes                                                   | Istream                                                                        |
|-----------|--------------------------------------------------------------|--------------------------------------------------------------------------------|
| Guardar      | [**MFGetAttributesAsBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob)       | [**MFSerializeAttributesToStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream)         |
| Cargar      | [**MFInitAttributesFromBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfinitattributesfromblob) | [**MFDeserializeAttributesFromStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream) |



 

Para escribir el contenido de un almacén de atributos en una matriz de bytes, llame a [**MFGetAttributesAsBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesasblob). Se **omiten los atributos con valores** de puntero IUnknown. Para volver a cargar los atributos en un almacén de atributos, llame a [**MFInitAttributesFromBlob**](/windows/desktop/api/mfapi/nf-mfapi-mfinitattributesfromblob).

Para escribir un almacén de atributos en una secuencia, llame a [**MFSerializeAttributesToStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfserializeattributestostream). Esta función puede serializar **valores de puntero IUnknown.** El autor de la llamada debe proporcionar un objeto de secuencia que implemente la **interfaz IStream.** Para cargar un almacén de atributos desde una secuencia, llame a [**MFDeserializeAttributesFromStream**](/windows/desktop/api/mfobjects/nf-mfobjects-mfdeserializeattributesfromstream).

## <a name="implementing-imfattributes"></a>Implementación deATTRIBUTEAttributes

Media Foundation proporciona una implementación de [**existencias deATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes), que se obtiene mediante una llamada a la [**función MFCreateAttributes.**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) En la mayoría de las situaciones, debe usar esta implementación y no proporcionar su propia implementación personalizada.

Hay una situación en la que es posible que tenga que implementar la interfaz [**DEATTRIBUTEAttributes:**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) si implementa una segunda interfaz que hereda **LOSATTRIBUTE.** En ese caso, debe proporcionar implementaciones para los **métodos DEATTRIBUTES heredados** por la segunda interfaz.

En esta situación, se recomienda ajustar la implementación de Media Foundation existente [**deATTRIBUTEAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes). En el código siguiente se muestra una plantilla de clase que contiene un puntero **DE TIPO IMFAttributes** y encapsula todos los **métodos IMFAttributes,** excepto **los métodos IUnknown.**


```C++
#include <assert.h>

// Helper class to implement IMFAttributes. 

// This is an abstract class; the derived class must implement the IUnknown 
// methods. This class is a wrapper for the standard attribute store provided 
// in Media Foundation.

// template parameter: 
// The interface you are implementing, either IMFAttributes or an interface 
// that inherits IMFAttributes, such as IMFActivate

template <class IFACE=IMFAttributes>
class CBaseAttributes : public IFACE
{
protected:
    IMFAttributes *m_pAttributes;

    // This version of the constructor does not initialize the 
    // attribute store. The derived class must call Initialize() in 
    // its own constructor.
    CBaseAttributes() : m_pAttributes(NULL)
    {
    }

    // This version of the constructor initializes the attribute 
    // store, but the derived class must pass an HRESULT parameter 
    // to the constructor.

    CBaseAttributes(HRESULT& hr, UINT32 cInitialSize = 0) : m_pAttributes(NULL)
    {
        hr = Initialize(cInitialSize);
    }

    // The next version of the constructor uses a caller-provided 
    // implementation of IMFAttributes.

    // (Sometimes you want to delegate IMFAttributes calls to some 
    // other object that implements IMFAttributes, rather than using 
    // MFCreateAttributes.)

    CBaseAttributes(HRESULT& hr, IUnknown *pUnk)
    {
        hr = Initialize(pUnk);
    }

    virtual ~CBaseAttributes()
    {
        if (m_pAttributes)
        {
            m_pAttributes->Release();
        }
    }

    // Initializes the object by creating the standard Media Foundation attribute store.
    HRESULT Initialize(UINT32 cInitialSize = 0)
    {
        if (m_pAttributes == NULL)
        {
            return MFCreateAttributes(&m_pAttributes, cInitialSize); 
        }
        else
        {
            return S_OK;
        }
    }

    // Initializes this object from a caller-provided attribute store.
    // pUnk: Pointer to an object that exposes IMFAttributes.
    HRESULT Initialize(IUnknown *pUnk)
    {
        if (m_pAttributes)
        {
            m_pAttributes->Release();
            m_pAttributes = NULL;
        }


        return pUnk->QueryInterface(IID_PPV_ARGS(&m_pAttributes));
    }

public:

    // IMFAttributes methods

    STDMETHODIMP GetItem(REFGUID guidKey, PROPVARIANT* pValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetItem(guidKey, pValue);
    }

    STDMETHODIMP GetItemType(REFGUID guidKey, MF_ATTRIBUTE_TYPE* pType)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetItemType(guidKey, pType);
    }

    STDMETHODIMP CompareItem(REFGUID guidKey, REFPROPVARIANT Value, BOOL* pbResult)
    {
        assert(m_pAttributes);
        return m_pAttributes->CompareItem(guidKey, Value, pbResult);
    }

    STDMETHODIMP Compare(
        IMFAttributes* pTheirs, 
        MF_ATTRIBUTES_MATCH_TYPE MatchType, 
        BOOL* pbResult
        )
    {
        assert(m_pAttributes);
        return m_pAttributes->Compare(pTheirs, MatchType, pbResult);
    }

    STDMETHODIMP GetUINT32(REFGUID guidKey, UINT32* punValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetUINT32(guidKey, punValue);
    }

    STDMETHODIMP GetUINT64(REFGUID guidKey, UINT64* punValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetUINT64(guidKey, punValue);
    }

    STDMETHODIMP GetDouble(REFGUID guidKey, double* pfValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetDouble(guidKey, pfValue);
    }

    STDMETHODIMP GetGUID(REFGUID guidKey, GUID* pguidValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetGUID(guidKey, pguidValue);
    }

    STDMETHODIMP GetStringLength(REFGUID guidKey, UINT32* pcchLength)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetStringLength(guidKey, pcchLength);
    }

    STDMETHODIMP GetString(REFGUID guidKey, LPWSTR pwszValue, UINT32 cchBufSize, UINT32* pcchLength)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetString(guidKey, pwszValue, cchBufSize, pcchLength);
    }

    STDMETHODIMP GetAllocatedString(REFGUID guidKey, LPWSTR* ppwszValue, UINT32* pcchLength)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetAllocatedString(guidKey, ppwszValue, pcchLength);
    }

    STDMETHODIMP GetBlobSize(REFGUID guidKey, UINT32* pcbBlobSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetBlobSize(guidKey, pcbBlobSize);
    }

    STDMETHODIMP GetBlob(REFGUID guidKey, UINT8* pBuf, UINT32 cbBufSize, UINT32* pcbBlobSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetBlob(guidKey, pBuf, cbBufSize, pcbBlobSize);
    }

    STDMETHODIMP GetAllocatedBlob(REFGUID guidKey, UINT8** ppBuf, UINT32* pcbSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetAllocatedBlob(guidKey, ppBuf, pcbSize);
    }

    STDMETHODIMP GetUnknown(REFGUID guidKey, REFIID riid, LPVOID* ppv)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetUnknown(guidKey, riid, ppv);
    }

    STDMETHODIMP SetItem(REFGUID guidKey, REFPROPVARIANT Value)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetItem(guidKey, Value);
    }

    STDMETHODIMP DeleteItem(REFGUID guidKey)
    {
        assert(m_pAttributes);
        return m_pAttributes->DeleteItem(guidKey);
    }

    STDMETHODIMP DeleteAllItems()
    {
        assert(m_pAttributes);
        return m_pAttributes->DeleteAllItems();
    }

    STDMETHODIMP SetUINT32(REFGUID guidKey, UINT32 unValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetUINT32(guidKey, unValue);
    }

    STDMETHODIMP SetUINT64(REFGUID guidKey,UINT64 unValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetUINT64(guidKey, unValue);
    }

    STDMETHODIMP SetDouble(REFGUID guidKey, double fValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetDouble(guidKey, fValue);
    }

    STDMETHODIMP SetGUID(REFGUID guidKey, REFGUID guidValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetGUID(guidKey, guidValue);
    }

    STDMETHODIMP SetString(REFGUID guidKey, LPCWSTR wszValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetString(guidKey, wszValue);
    }

    STDMETHODIMP SetBlob(REFGUID guidKey, const UINT8* pBuf, UINT32 cbBufSize)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetBlob(guidKey, pBuf, cbBufSize);
    }

    STDMETHODIMP SetUnknown(REFGUID guidKey, IUnknown* pUnknown)
    {
        assert(m_pAttributes);
        return m_pAttributes->SetUnknown(guidKey, pUnknown);
    }

    STDMETHODIMP LockStore()
    {
        assert(m_pAttributes);
        return m_pAttributes->LockStore();
    }

    STDMETHODIMP UnlockStore()
    {
        assert(m_pAttributes);
        return m_pAttributes->UnlockStore();
    }

    STDMETHODIMP GetCount(UINT32* pcItems)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetCount(pcItems);
    }

    STDMETHODIMP GetItemByIndex(UINT32 unIndex, GUID* pguidKey, PROPVARIANT* pValue)
    {
        assert(m_pAttributes);
        return m_pAttributes->GetItemByIndex(unIndex, pguidKey, pValue);
    }

    STDMETHODIMP CopyAllItems(IMFAttributes* pDest)
    {
        assert(m_pAttributes);
        return m_pAttributes->CopyAllItems(pDest);
    }

    // Helper functions
    
    HRESULT SerializeToStream(DWORD dwOptions, IStream* pStm)      
        // dwOptions: Flags from MF_ATTRIBUTE_SERIALIZE_OPTIONS
    {
        assert(m_pAttributes);
        return MFSerializeAttributesToStream(m_pAttributes, dwOptions, pStm);
    }

    HRESULT DeserializeFromStream(DWORD dwOptions, IStream* pStm)
    {
        assert(m_pAttributes);
        return MFDeserializeAttributesFromStream(m_pAttributes, dwOptions, pStm);
    }

    // SerializeToBlob: Stores the attributes in a byte array. 
    // 
    // ppBuf: Receives a pointer to the byte array. 
    // pcbSize: Receives the size of the byte array.
    //
    // The caller must free the array using CoTaskMemFree.
    HRESULT SerializeToBlob(UINT8 **ppBuffer, UINT32 *pcbSize)
    {
        assert(m_pAttributes);

        if (ppBuffer == NULL)
        {
            return E_POINTER;
        }
        if (pcbSize == NULL)
        {
            return E_POINTER;
        }

        *ppBuffer = NULL;
        *pcbSize = 0;

        UINT32 cbSize = 0;
        BYTE *pBuffer = NULL;

        HRESULT hr = MFGetAttributesAsBlobSize(m_pAttributes, &cbSize);

        if (FAILED(hr))
        {
            return hr;
        }

        pBuffer = (BYTE*)CoTaskMemAlloc(cbSize);
        if (pBuffer == NULL)
        {
            return E_OUTOFMEMORY;
        }

        hr = MFGetAttributesAsBlob(m_pAttributes, pBuffer, cbSize);

        if (SUCCEEDED(hr))
        {
            *ppBuffer = pBuffer;
            *pcbSize = cbSize;
        }
        else
        {
            CoTaskMemFree(pBuffer);
        }
        return hr;
    }
    
    HRESULT DeserializeFromBlob(const UINT8* pBuffer, UINT cbSize)
    {
        assert(m_pAttributes);
        return MFInitAttributesFromBlob(m_pAttributes, pBuffer, cbSize);
    }

    HRESULT GetRatio(REFGUID guidKey, UINT32* pnNumerator, UINT32* punDenominator)
    {
        assert(m_pAttributes);
        return MFGetAttributeRatio(m_pAttributes, guidKey, pnNumerator, punDenominator);
    }

    HRESULT SetRatio(REFGUID guidKey, UINT32 unNumerator, UINT32 unDenominator)
    {
        assert(m_pAttributes);
        return MFSetAttributeRatio(m_pAttributes, guidKey, unNumerator, unDenominator);
    }

    // Gets an attribute whose value represents the size of something (eg a video frame).
    HRESULT GetSize(REFGUID guidKey, UINT32* punWidth, UINT32* punHeight)
    {
        assert(m_pAttributes);
        return MFGetAttributeSize(m_pAttributes, guidKey, punWidth, punHeight);
    }

    // Sets an attribute whose value represents the size of something (eg a video frame).
    HRESULT SetSize(REFGUID guidKey, UINT32 unWidth, UINT32 unHeight)
    {
        assert(m_pAttributes);
        return MFSetAttributeSize (m_pAttributes, guidKey, unWidth, unHeight);
    }
};
```



El código siguiente muestra cómo derivar una clase de esta plantilla:


```C++
#include <shlwapi.h>

class MyObject : public CBaseAttributes<>
{
    MyObject() : m_nRefCount(1) { }
    ~MyObject() { }

    long m_nRefCount;

public:

    // IUnknown
    STDMETHODIMP MyObject::QueryInterface(REFIID riid, void** ppv)
    {
        static const QITAB qit[] = 
        {
            QITABENT(MyObject, IMFAttributes),
            { 0 },
        };
        return QISearch(this, qit, riid, ppv);
    }

    STDMETHODIMP_(ULONG) MyObject::AddRef()
    {
        return InterlockedIncrement(&m_nRefCount);
    }

    STDMETHODIMP_(ULONG) MyObject::Release()
    {
        ULONG uCount = InterlockedDecrement(&m_nRefCount);
        if (uCount == 0)
        {
            delete this;
        }
        return uCount;
    }

    // Static function to create an instance of the object.

    static HRESULT CreateInstance(MyObject **ppObject)
    {
        HRESULT hr = S_OK;

        MyObject *pObject = new MyObject();
        if (pObject == NULL)
        {
            return E_OUTOFMEMORY;
        }

        // Initialize the attribute store.
        hr = pObject->Initialize();

        if (FAILED(hr))
        {
            delete pObject;
            return hr;
        }

        *ppObject = pObject;
        (*ppObject)->AddRef();

        return S_OK;
    }
};
```



Debe llamar a `CBaseAttributes::Initialize` para crear el almacén de atributos. En el ejemplo anterior, esto se hace dentro de una función de creación estática.

El argumento de plantilla es un tipo de interfaz, cuyo valor predeterminado [**es IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes). Si el objeto implementa una interfaz que hereda **DEATTRIBUTEAttributes**, como [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate), establezca el argumento de plantilla igual al nombre de la interfaz derivada.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Media Foundation primitivos](media-foundation-primitives.md)
</dt> </dl>

 

 



