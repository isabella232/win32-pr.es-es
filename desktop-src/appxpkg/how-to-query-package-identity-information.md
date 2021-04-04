---
title: Información del manifiesto del paquete de la aplicación de consulta (C++)
description: Obtenga información sobre cómo obtener información del manifiesto del paquete de aplicaciones para una aplicación de Windows mediante la API de empaquetado.
ms.assetid: A29986F9-C620-48CD-87F8-525DFA076AAB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9940f92a4412be7731db2454d68b4429522b63f6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "104077574"
---
# <a name="query-app-package-manifest-info-c"></a><span data-ttu-id="d5b41-103">Información del manifiesto del paquete de la aplicación de consulta (C++)</span><span class="sxs-lookup"><span data-stu-id="d5b41-103">Query app package manifest info (C++)</span></span>

<span data-ttu-id="d5b41-104">Obtenga información sobre cómo obtener información del manifiesto del paquete de aplicaciones para una aplicación de Windows mediante la [API de empaquetado](interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="d5b41-104">Learn how to get info from the app package manifest for a Windows app using the [packaging API](interfaces.md).</span></span>

### <a name="create-a-package-manifest-reader"></a><span data-ttu-id="d5b41-105">Crear un lector de manifiestos de paquete</span><span class="sxs-lookup"><span data-stu-id="d5b41-105">Create a package manifest reader</span></span>

<span data-ttu-id="d5b41-106">Para crear un lector de manifiestos de paquete, llame a [**IAppxFactory:: CreatePackageReader**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfactory-createpackagereader) para crear un lector de paquetes.</span><span class="sxs-lookup"><span data-stu-id="d5b41-106">To create a package manifest reader, call [**IAppxFactory::CreatePackageReader**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxfactory-createpackagereader) to create a package reader.</span></span> <span data-ttu-id="d5b41-107">El primer parámetro es un flujo de entrada para el paquete (archivo. appx).</span><span class="sxs-lookup"><span data-stu-id="d5b41-107">The first parameter is an input stream for the package (.appx file).</span></span> <span data-ttu-id="d5b41-108">El segundo parámetro es un parámetro de salida que recibe un puntero a un puntero [**IAppxPackageReader**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxpackagereader) .</span><span class="sxs-lookup"><span data-stu-id="d5b41-108">The second parameter is an output parameter that receives a pointer to an [**IAppxPackageReader**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxpackagereader) pointer.</span></span> <span data-ttu-id="d5b41-109">A continuación, llame a [**IAppxPackageReader:: GetManifest**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagereader-getmanifest) para obtener el lector del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="d5b41-109">Next, call [**IAppxPackageReader::GetManifest**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxpackagereader-getmanifest) to get the manifest reader.</span></span> <span data-ttu-id="d5b41-110">El parámetro es un parámetro de salida que recibe un puntero a un puntero [**IAppxManifestReader**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestreader) .</span><span class="sxs-lookup"><span data-stu-id="d5b41-110">The parameter is an output parameter that receives a pointer to an [**IAppxManifestReader**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestreader) pointer.</span></span>


```C++
int wmain(
    _In_ int argc,
    _In_reads_(argc) wchar_t** argv)
{
    HRESULT hr = S_OK;
 
    if (argc != 2)
    {
        wprintf(L"Usage: DescribeAppx.exe inputFile\n");
        wprintf(L"       inputFile: Path to the app package to read\n");
        return 2;
    }

    // Specify the appropriate COM threading model
    hr = CoInitializeEx(NULL, COINIT_MULTITHREADED);

    if (SUCCEEDED(hr))
    {
        IAppxPackageReader* packageReader = NULL;
        IAppxManifestReader* manifestReader = NULL;

        // Create a package reader using the file name given in command line
        hr = GetPackageReader(argv[1], &packageReader);

        // Get manifest reader for the package and read from the manifest
        if (SUCCEEDED(hr))
        {
            hr = packageReader->GetManifest(&manifestReader);
        }
        if (SUCCEEDED(hr))
        {
            hr = ReadManifest(manifestReader);
        }
    }
}

//
// Creates an app package reader.
//
// Parameters:
//   inputFileName 
//     Fully qualified name of the app package (.appx file) to be opened.
//   reader 
//     On success, receives the created instance of IAppxPackageReader.
//
HRESULT GetPackageReader(
    _In_ LPCWSTR inputFileName,
    _Outptr_ IAppxPackageReader** reader)
{
    HRESULT hr = S_OK;
    IAppxFactory* appxFactory = NULL;
    IStream* inputStream = NULL;

    // Create a new factory
    hr = CoCreateInstance(
            __uuidof(AppxFactory),
            NULL,
            CLSCTX_INPROC_SERVER,
            __uuidof(IAppxFactory),
            (LPVOID*)(&appxFactory));

    // Create a stream over the input app package
    if (SUCCEEDED(hr))
    {
        hr = SHCreateStreamOnFileEx(
                inputFileName,
                STGM_READ | STGM_SHARE_EXCLUSIVE,
                0, // default file attributes
                FALSE, // do not create new file
                NULL, // no template
                &inputStream);
    }

    // Create a new package reader using the factory.  For 
    // simplicity, we don't verify the digital signature of the package.
    if (SUCCEEDED(hr))
    {
        hr = appxFactory->CreatePackageReader(
                inputStream,
                reader);
    }

    // Clean up allocated resources
    if (inputStream != NULL)
    {
        inputStream->Release();
        inputStream = NULL;
    }
    if (appxFactory != NULL)
    {
        appxFactory->Release();
        appxFactory = NULL;
    }
    return hr;
}
```



### <a name="read-package-identity-info"></a><span data-ttu-id="d5b41-111">Leer información de identidad del paquete</span><span class="sxs-lookup"><span data-stu-id="d5b41-111">Read package identity info</span></span>

<span data-ttu-id="d5b41-112">La identificación del paquete se especifica mediante el elemento [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) del manifiesto.</span><span class="sxs-lookup"><span data-stu-id="d5b41-112">Package identify is specified using the [**Identity**](/uwp/schemas/appxpackage/appxmanifestschema/element-identity) element in the manifest.</span></span> <span data-ttu-id="d5b41-113">Use [**IAppxManifestReader:: GetPackageId**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getpackageid) para obtener un [**IAppxManifestPackageId**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestpackageid) para leer la información de identidad del paquete, como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="d5b41-113">Use [**IAppxManifestReader::GetPackageId**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getpackageid) to get an [**IAppxManifestPackageId**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestpackageid) to read package identity info, as shown here.</span></span>

<span data-ttu-id="d5b41-114">Este código usa [**IAppxManifestPackageId:: GetPackageFullName**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getpackagefullname) para obtener el nombre completo del paquete, [**IAppxManifestPackageId:: GetName**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getname) para obtener el nombre del paquete y [**IAppxManifestPackageId:: GetVersion**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getversion) para obtener la versión del paquete.</span><span class="sxs-lookup"><span data-stu-id="d5b41-114">This code uses [**IAppxManifestPackageId::GetPackageFullName**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getpackagefullname) to get the package full name, [**IAppxManifestPackageId::GetName**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getname) to get the package name, and [**IAppxManifestPackageId::GetVersion**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestpackageid-getversion) to get the package version.</span></span>


```C++
//
// Reads a subset of the manifest Identity element.
//
//
HRESULT ReadManifestPackageId(
    _In_ IAppxManifestReader* manifestReader)
{
    HRESULT hr = S_OK;

    IAppxManifestPackageId* packageId = NULL;

    // Get elements and attributes from the manifest reader
    hr = manifestReader->GetPackageId(&packageId);
    if (SUCCEEDED(hr))
    {
        LPWSTR packageFullName = NULL;
        LPWSTR packageName = NULL;
        UINT64 packageVersion = 0;

        hr = packageId->GetPackageFullName(&packageFullName);

        if (SUCCEEDED(hr))
        {
            hr = packageId->GetName(&packageName);
        }
        if (SUCCEEDED(hr))
        {
            hr = packageId->GetVersion(&packageVersion);
        }
        if (SUCCEEDED(hr))
        {
            wprintf(L"Package full name: %s\n", packageFullName);
            wprintf(L"Package name: %s\n", packageName);
            wprintf(L"Package version: ");

            // Convert version number from 64-bit integer to dot-quad form
            for (int bitPosition = 0x30; bitPosition >= 0; bitPosition -= 0x10)
            {
                UINT64 versionWord = (packageVersion >> bitPosition) & 0xFFFF;
                wprintf(L"%llu.", versionWord);
            }
            wprintf(L"\n");
        }

        // Free all string buffers returned from the manifest API
        CoTaskMemFree(packageFullName);
        CoTaskMemFree(packageName);
    }

    // Clean up allocated resources
    if (packageId != NULL)
    {
        packageId->Release();
        packageId = NULL;
    }
     
    return hr;
}
```



### <a name="read-metadata-that-describes-the-package-to-users"></a><span data-ttu-id="d5b41-115">Leer metadatos que describen el paquete para los usuarios</span><span class="sxs-lookup"><span data-stu-id="d5b41-115">Read metadata that describes the package to users</span></span>

<span data-ttu-id="d5b41-116">Las propiedades se especifican mediante el elemento [**Properties**](/uwp/schemas/appxpackage/appxmanifestschema/element-properties) en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="d5b41-116">Properties are specified using the [**Properties**](/uwp/schemas/appxpackage/appxmanifestschema/element-properties) element in the manifest.</span></span> <span data-ttu-id="d5b41-117">Use [**IAppxManifestReader:: GetProperties**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getproperties) para obtener un [**IAppxManifestProperties**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestproperties) para leer este nodo, como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="d5b41-117">Use [**IAppxManifestReader::GetProperties**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getproperties) to get an [**IAppxManifestProperties**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestproperties) to read this node, as shown here.</span></span>

<span data-ttu-id="d5b41-118">Este código usa [**IAppxManifestProperties:: GetStringValue**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestproperties-getstringvalue) para obtener el nombre para mostrar del paquete y la descripción del paquete.</span><span class="sxs-lookup"><span data-stu-id="d5b41-118">This code uses [**IAppxManifestProperties::GetStringValue**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestproperties-getstringvalue) to get the package display name and package description.</span></span>


```C++
//
// Reads a subset of the manifest Properties element.
//
//
HRESULT ReadManifestProperties(
    _In_ IAppxManifestReader* manifestReader)
{
    HRESULT hr = S_OK;

    IAppxManifestProperties* properties = NULL;

    // Get elements and attributes from the manifest reader
    hr = manifestReader->GetProperties(&properties);
    if (SUCCEEDED(hr))
    {
        LPWSTR displayName = NULL;
        LPWSTR description = NULL;

        hr = properties->GetStringValue(L"DisplayName", &displayName);

        if (SUCCEEDED(hr))
        {
            hr = properties->GetStringValue(L"Description", &description);
        }
        if (SUCCEEDED(hr))
        {
            wprintf(L"Package display name: %s\n", displayName);
            wprintf(L"Package description:  %s\n", description);
        }

        // Free all string buffers returned from the manifest API
        CoTaskMemFree(displayName);
        CoTaskMemFree(description);
    }
    // Clean up allocated resources
    if (properties != NULL)
    {
        properties->Release();
        properties = NULL;
    }

    return hr;
}
```



### <a name="read-metadata-about-the-apps-included-in-the-package"></a><span data-ttu-id="d5b41-119">Leer metadatos acerca de las aplicaciones incluidas en el paquete</span><span class="sxs-lookup"><span data-stu-id="d5b41-119">Read metadata about the apps included in the package</span></span>

<span data-ttu-id="d5b41-120">Las aplicaciones se especifican mediante el elemento [**Applications**](/uwp/schemas/appxpackage/appxmanifestschema/element-applications) en el manifiesto.</span><span class="sxs-lookup"><span data-stu-id="d5b41-120">Apps are specified using the [**Applications**](/uwp/schemas/appxpackage/appxmanifestschema/element-applications) element in the manifest.</span></span> <span data-ttu-id="d5b41-121">Use [**IAppxManifestReader:: GetApplications**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getapplications) para obtener un [**IAppxManifestApplicationsEnumerator**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestapplicationsenumerator) para leer este nodo.</span><span class="sxs-lookup"><span data-stu-id="d5b41-121">Use [**IAppxManifestReader::GetApplications**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestreader-getapplications) to get an [**IAppxManifestApplicationsEnumerator**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestapplicationsenumerator) to read this node.</span></span> <span data-ttu-id="d5b41-122">Use [**IAppxManifestApplicationsEnumerator:: GetCurrent**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplicationsenumerator-getcurrent) y [**IAppxManifestApplicationsEnumerator:: MoveNext**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplicationsenumerator-movenext) para obtener un [**IAppxManifestApplication**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestapplication) para cada aplicación del paquete.</span><span class="sxs-lookup"><span data-stu-id="d5b41-122">Use [**IAppxManifestApplicationsEnumerator::GetCurrent**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplicationsenumerator-getcurrent) and [**IAppxManifestApplicationsEnumerator::MoveNext**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplicationsenumerator-movenext) to get an [**IAppxManifestApplication**](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestapplication) for each app in the package.</span></span>

<span data-ttu-id="d5b41-123">Este código usa [**IAppxManifestApplication:: GetStringValue**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplication-getstringvalue) para obtener el nombre para mostrar de cada aplicación.</span><span class="sxs-lookup"><span data-stu-id="d5b41-123">This code uses [**IAppxManifestApplication::GetStringValue**](/windows/desktop/api/AppxPackaging/nf-appxpackaging-iappxmanifestapplication-getstringvalue) to get the display name for each app.</span></span>


```C++
//
// Reads a subset of the manifest Applications element.
//
//
HRESULT ReadManifestApplications(
    _In_ IAppxManifestReader* manifestReader)
{
    HRESULT hr = S_OK;
    BOOL hasCurrent = FALSE;
    UINT32 applicationsCount = 0;

    IAppxManifestApplicationsEnumerator* applications = NULL;

    // Get elements and attributes from the manifest reader
    hr = manifestReader->GetApplications(&applications);
    if (SUCCEEDED(hr))
    {
        hr = applications->GetHasCurrent(&hasCurrent);

        while (SUCCEEDED(hr) && hasCurrent)
        {
            IAppxManifestApplication* application = NULL;
            LPWSTR applicationName = NULL;

            hr = applications->GetCurrent(&application);
            if (SUCCEEDED(hr))
            {
                application->GetStringValue(L"DisplayName", &applicationName);
            }
            if (SUCCEEDED(hr))
            {
                applicationsCount++;
                wprintf(L"App #%u: %s\n", applicationsCount, applicationName);
            }

            if (SUCCEEDED(hr))
            {
                hr = applications->MoveNext(&hasCurrent);
            }
            if (application != NULL)
            {
                application->Release();
                application = NULL;
            }
            CoTaskMemFree(applicationName);
        }

        wprintf(L"Count of apps in the package: %u\n", applicationsCount);
    }

    // Clean up allocated resources
    if (applications != NULL)
    {
        applications->Release();
        applications = NULL;
    }

    return hr;
}
```



### <a name="clean-up-the-package-manifest-reader"></a><span data-ttu-id="d5b41-124">Limpiar el lector del manifiesto del paquete</span><span class="sxs-lookup"><span data-stu-id="d5b41-124">Clean up the package manifest reader</span></span>

<span data-ttu-id="d5b41-125">Antes de volver de la `wmain` función, llame al método [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) para limpiar el lector del manifiesto del paquete y llamar a la función [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) .</span><span class="sxs-lookup"><span data-stu-id="d5b41-125">Before returning from the `wmain` function, call the [**Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) method to clean up the package manifest reader and call the [**CoUninitialize**](/windows/desktop/api/combaseapi/nf-combaseapi-couninitialize) function.</span></span>


```C++
// Clean up allocated resources
if (manifestReader != NULL)
{
    manifestReader->Release();
    manifestReader = NULL;
}
if (packageReader != NULL)
{
    packageReader->Release();
    packageReader = NULL;
}

CoUninitialize();
```



## <a name="related-topics"></a><span data-ttu-id="d5b41-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="d5b41-126">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d5b41-127">**Ejemplos**</span><span class="sxs-lookup"><span data-stu-id="d5b41-127">**Samples**</span></span>
</dt> <dt>

[<span data-ttu-id="d5b41-128">Ejemplo de paquete de aplicación de consulta y manifiesto de aplicación</span><span class="sxs-lookup"><span data-stu-id="d5b41-128">Query app package and app manifest sample</span></span>](https://github.com/microsoft/Windows-classic-samples/tree/master/Samples/AppxPackingDescribeAppx)
</dt> <dt>

<span data-ttu-id="d5b41-129">**Referencia**</span><span class="sxs-lookup"><span data-stu-id="d5b41-129">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="d5b41-130">**IAppxManifestReader**</span><span class="sxs-lookup"><span data-stu-id="d5b41-130">**IAppxManifestReader**</span></span>](/windows/desktop/api/AppxPackaging/nn-appxpackaging-iappxmanifestreader)
</dt> </dl>

 

 