---
description: Proporciona acceso de lectura a un archivo de Windows Journal y devuelve una secuencia que contiene una versión XML del contenido del archivo.
ms.assetid: e4e19f69-6377-4f06-856d-7f9b453e7656
title: Interfaz IJournalReader (Journal. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IJournalReader
api_type:
- COM
api_location:
- Journal.dll
ms.openlocfilehash: 7576996d341f13518879310f08c0a48996e1293f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361581"
---
# <a name="ijournalreader-interface"></a><span data-ttu-id="9983b-103">Interfaz IJournalReader</span><span class="sxs-lookup"><span data-stu-id="9983b-103">IJournalReader interface</span></span>

<span data-ttu-id="9983b-104">Proporciona acceso de lectura a un archivo de Windows Journal y devuelve una secuencia que contiene una versión XML del contenido del archivo.</span><span class="sxs-lookup"><span data-stu-id="9983b-104">Provides read access to a Windows Journal file, returning a stream containing an XML version of the file's contents.</span></span>

> [!Note]  
> <span data-ttu-id="9983b-105">El componente lector del diario no puede leer archivos de Windows Journal creados por equipos que ejecutan Windows 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="9983b-105">The Journal Reader component cannot read Windows Journal files created by machines running Windows 7 or later.</span></span> <span data-ttu-id="9983b-106">La interfaz IJournalReader se debe considerar en desuso u obsoleta y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="9983b-106">The IJournalReader interface should be considered deprecated or obsolete and should not be used.</span></span>

 

## <a name="members"></a><span data-ttu-id="9983b-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9983b-107">Members</span></span>

<span data-ttu-id="9983b-108">La interfaz **IJournalReader** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9983b-108">The **IJournalReader** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9983b-109">**IJournalReader** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9983b-109">**IJournalReader** also has these types of members:</span></span>

-   [<span data-ttu-id="9983b-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="9983b-110">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9983b-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="9983b-111">Methods</span></span>

<span data-ttu-id="9983b-112">La interfaz **IJournalReader** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="9983b-112">The **IJournalReader** interface has these methods.</span></span>



| <span data-ttu-id="9983b-113">Método</span><span class="sxs-lookup"><span data-stu-id="9983b-113">Method</span></span>                                                  | <span data-ttu-id="9983b-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="9983b-114">Description</span></span>                                                                                                           |
|:--------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9983b-115">**ReadFromStream**</span><span class="sxs-lookup"><span data-stu-id="9983b-115">**ReadFromStream**</span></span>](ijournalreader-readfromstream.md) | <span data-ttu-id="9983b-116">Toma un flujo a un archivo de notas de Journal y devuelve una secuencia XML que representa el contenido del documento.</span><span class="sxs-lookup"><span data-stu-id="9983b-116">Takes a stream to a Journal Note file and returns an XML stream representing the contents of the document.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9983b-117">Observaciones</span><span class="sxs-lookup"><span data-stu-id="9983b-117">Remarks</span></span>

<span data-ttu-id="9983b-118">La clase **JournalReader** permite cargar un flujo de documento de diario y recibir una secuencia XML que representa el contenido.</span><span class="sxs-lookup"><span data-stu-id="9983b-118">The **JournalReader** class enables you to load a Journal document stream and to receive an XML stream representing the contents.</span></span> <span data-ttu-id="9983b-119">Puede reconstituir, mostrar y manipular la tinta.</span><span class="sxs-lookup"><span data-stu-id="9983b-119">You can reconstitute, display, and manipulate the ink.</span></span>

## <a name="examples"></a><span data-ttu-id="9983b-120">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="9983b-120">Examples</span></span>

<span data-ttu-id="9983b-121">En el ejemplo siguiente de un controlador del evento [**click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) de un botón se crea una instancia de la clase **JournalReader** y se usa para leer un archivo de diario existente.</span><span class="sxs-lookup"><span data-stu-id="9983b-121">The following example of a handler for a button's [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) event creates an instance of the **JournalReader** class and uses it to read an existing Journal file.</span></span>

> [!Note]  
> <span data-ttu-id="9983b-122">No se muestra el método **DisplayXml** al que se llama desde este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="9983b-122">The **DisplayXml** method called from this example is not shown.</span></span> <span data-ttu-id="9983b-123">La implementación específica de este tipo de método depende de las necesidades de la aplicación.</span><span class="sxs-lookup"><span data-stu-id="9983b-123">The specific implementation of such a method is dependent on your application's needs.</span></span>

 


```C++
void CJntlReaderMFCDlg::OnBnClickedButton1()
{
  static TCHAR BASED_CODE szFilter[] = 
    _T("Journal files (*.jnt)|*.jnt|All files (*.*)|*.*");
  CFileDialog* fileDialog = new CFileDialog(TRUE, _T("*.jnt"), NULL, 
                                 OFN_FILEMUSTEXIST, szFilter, this);

  // Get the filename from the user via a File Open dialog
  if (fileDialog != NULL &&
      fileDialog->DoModal() == IDOK)
  {
    CString strFileName = fileDialog->GetPathName();

    // Read a JNT file into a memory buffer
    HANDLE hFile = CreateFile(strFileName,
                              GENERIC_READ,
                              FILE_SHARE_READ,
                              NULL,
                              OPEN_EXISTING,
                              FILE_ATTRIBUTE_NORMAL,
                              NULL);
    
    if (hFile != INVALID_HANDLE_VALUE)
    {
      // Allocate memory to hold the file contents
      DWORD dwFileSize = GetFileSize(hFile, NULL);
      HGLOBAL hGlobal = GlobalAlloc(GHND, dwFileSize);

      if (hGlobal != NULL)
      {
        LPBYTE pData = (LPBYTE)GlobalLock(hGlobal);

        if (pData != NULL)
        {
          DWORD dwRead;

          // Read the Journal file into the pData buffer
          if (ReadFile(hFile, pData, dwFileSize, &dwRead, NULL) &&
              (dwRead == dwFileSize))
          {
            HRESULT hr;
            IStream* pJntStream;

            // Create an IStream that points to the buffer
            hr = CreateStreamOnHGlobal(hGlobal, FALSE, &pJntStream);

            if (SUCCEEDED(hr))
            {
              IJournalReader* pJntReader;

              // Create a JournalReader object
              hr = CoCreateInstance(CLSID_JournalReader, NULL, CLSCTX_ALL, 
                          IID_IJournalReader, (void**)&pJntReader);

              if (SUCCEEDED(hr))
              {
                IStream* pXmlStream;

                // Read in the JNT file via the JournalReader
                hr = pJntReader->ReadFromStream(pJntStream, &pXmlStream);

                if (SUCCEEDED(hr))
                {
                  // Display results
                  DisplayXml(pXmlStream);

                  // Clean up
                  pXmlStream->Release();
                }
                pJntReader->Release();
              }
              pJntStream->Release();
            }
          }
          GlobalUnlock(hGlobal);
        }
        GlobalFree(hGlobal);
      }
      CloseHandle(hFile);
    }
    delete fileDialog;
  }
}
```



## <a name="requirements"></a><span data-ttu-id="9983b-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9983b-124">Requirements</span></span>



| <span data-ttu-id="9983b-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="9983b-125">Requirement</span></span> | <span data-ttu-id="9983b-126">Value</span><span class="sxs-lookup"><span data-stu-id="9983b-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9983b-127">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9983b-127">Minimum supported client</span></span><br/> | <span data-ttu-id="9983b-128">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="9983b-128">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="9983b-129">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9983b-129">Minimum supported server</span></span><br/> | <span data-ttu-id="9983b-130">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9983b-130">None supported</span></span><br/>                                                                                         |
| <span data-ttu-id="9983b-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9983b-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="9983b-132"><dt>Journal. h (también requiere Journal \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="9983b-132"><dt>Journal.h (also requires journal\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="9983b-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9983b-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9983b-134"><dt>Journal.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9983b-134"><dt>Journal.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="9983b-135">Vea también</span><span class="sxs-lookup"><span data-stu-id="9983b-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9983b-136">GUID de propiedad personalizada</span><span class="sxs-lookup"><span data-stu-id="9983b-136">Custom Property GUIDs</span></span>](custom-property-guids.md)
</dt> <dt>

[<span data-ttu-id="9983b-137">**Método ReadFromStream**</span><span class="sxs-lookup"><span data-stu-id="9983b-137">**ReadFromStream Method**</span></span>](ijournalreader-readfromstream.md)
</dt> </dl>

 

