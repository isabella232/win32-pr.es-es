---
description: Toma un flujo a un archivo de notas de Journal y devuelve una secuencia XML que representa el contenido del documento.
ms.assetid: 5a169dfe-b102-4aef-9efe-5db2cd2fb96f
title: 'IJournalReader:: ReadFromStream (método) (Journal. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IJournalReader.ReadFromStream
api_type:
- COM
api_location:
- Journal.dll
ms.openlocfilehash: 258ac30b8857fa4ef24bd86a08c7e402229f4bff
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105696250"
---
# <a name="ijournalreaderreadfromstream-method"></a><span data-ttu-id="5ca87-103">IJournalReader:: ReadFromStream (método)</span><span class="sxs-lookup"><span data-stu-id="5ca87-103">IJournalReader::ReadFromStream method</span></span>

<span data-ttu-id="5ca87-104">Toma un flujo a un archivo de notas de Journal y devuelve una secuencia XML que representa el contenido del documento.</span><span class="sxs-lookup"><span data-stu-id="5ca87-104">Takes a stream to a Journal Note file and returns an XML stream representing the contents of the document.</span></span>

> [!Note]  
> <span data-ttu-id="5ca87-105">El componente lector del diario no puede leer archivos de Windows Journal creados por equipos que ejecutan Windows 7 o posterior.</span><span class="sxs-lookup"><span data-stu-id="5ca87-105">The Journal Reader component cannot read Windows Journal files created by machines running Windows 7 or later.</span></span> <span data-ttu-id="5ca87-106">La interfaz IJournalReader se debe considerar en desuso u obsoleta y no debe usarse.</span><span class="sxs-lookup"><span data-stu-id="5ca87-106">The IJournalReader interface should be considered deprecated or obsolete and should not be used.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5ca87-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5ca87-107">Syntax</span></span>


```C++
HRESULT ReadFromStream(
  [in]          IStream *pJournalFileStream,
  [out, retval] IStream **ppXmlStream
);
```



## <a name="parameters"></a><span data-ttu-id="5ca87-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5ca87-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ca87-109">*pJournalFileStream* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="5ca87-109">*pJournalFileStream* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca87-110">Objeto [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) que representa el archivo de diario que se va a leer.</span><span class="sxs-lookup"><span data-stu-id="5ca87-110">An [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) object representing the Journal file to read.</span></span>

</dd> <dt>

<span data-ttu-id="5ca87-111">*ppXmlStream* \[ out, retval\]</span><span class="sxs-lookup"><span data-stu-id="5ca87-111">*ppXmlStream* \[out, retval\]</span></span>
</dt> <dd>

<span data-ttu-id="5ca87-112">Un puntero a la dirección de un objeto [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) que recibirá el flujo XML creado mediante la lectura del archivo de diario.</span><span class="sxs-lookup"><span data-stu-id="5ca87-112">A pointer to the address of an [**IStream**](/windows/desktop/api/objidl/nn-objidl-istream) object that will receive the XML stream created by reading the Journal file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ca87-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5ca87-113">Return value</span></span>

<span data-ttu-id="5ca87-114">Si este método se ejecuta correctamente, devuelve **S \_ correcto**.</span><span class="sxs-lookup"><span data-stu-id="5ca87-114">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5ca87-115">De lo contrario, devuelve un código de error **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5ca87-115">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="5ca87-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="5ca87-116">Remarks</span></span>

<span data-ttu-id="5ca87-117">Las secuencias se utilizan para evitar el acceso directo al sistema de archivos y para permitir la elección del método de análisis de XML que se va a usar.</span><span class="sxs-lookup"><span data-stu-id="5ca87-117">Streams are used to avoid direct access to the file system and to allow choice in which XML parsing method to use.</span></span>

## <a name="examples"></a><span data-ttu-id="5ca87-118">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="5ca87-118">Examples</span></span>

<span data-ttu-id="5ca87-119">En el ejemplo siguiente de un controlador del evento [**click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) de un botón se crea una instancia de la interfaz de la [**interfaz IJournalReader**](ijournalreader.md) y se usa para leer un archivo de diario existente.</span><span class="sxs-lookup"><span data-stu-id="5ca87-119">The following example of a handler for a button's [**Click**](/dotnet/api/system.windows.forms.control.click?view=netcore-3.1) event creates an instance of the [**IJournalReader Interface**](ijournalreader.md) interface and uses it to read an existing Journal file.</span></span>


```C++
void CJntlReaderMFCDlg::OnBnClickedButton1()
{
  IStream* pJntStream;
  IStream* pXmlStream;
  IJournalReader* pJntReader;
  HRESULT hr;
  CString szFileName = "";
  static char BASED_CODE szFilter[] = 
    "Journal files (*.jnt)|*.jnt|All files (*.*)|*.*";
  CFileDialog* fileDialog = new CFileDialog(TRUE, "*.jnt", NULL, 
                                 OFN_FILEMUSTEXIST, szFilter, this);

  // Get the filename from the user by using a File Open dialog
  if (IDOK == fileDialog->DoModal())
  {
    szFileName = fileDialog->GetPathName();

    // Read a JNT file into a memory buffer
    HANDLE hFile = CreateFile(szFileName.GetBuffer(), GENERIC_READ, FILE_SHARE_READ, NULL, OPEN_EXISTING, FILE_ATTRIBUTE_NORMAL, NULL);
    
    if (INVALID_HANDLE_VALUE != hFile)
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
          if (ReadFile(hFile, pData, dwFileSize, &dwRead, NULL) && dwRead == dwFileSize)
          {
            // Create an IStream that points to the buffer
            hr = CreateStreamOnHGlobal(hGlobal, FALSE, &pJntStream);

            if (SUCCEEDED(hr))
            {
              // Create a JournalReader object
              hr = CoCreateInstance(CLSID_JournalReader, NULL, CLSCTX_ALL, 
                          IID_IJournalReader, (void**)&pJntReader);

              if (SUCCEEDED(hr))
              {
                // Read in the JNT file by using the JournalReader
                hr = pJntReader->ReadFromStream(pJntStream, &pXmlStream);

                // Display results
                if (SUCCEEDED(hr))
                {
                  DisplayXml(pXmlStream);
                }

                // Clean up
                pXmlStream->Release();
                pJntReader = NULL;
                pJntStream->Release();
              }
            }
          }
          GlobalUnlock(hGlobal);
        }
        GlobalFree(hGlobal);
      }
    }
  }
}
```



## <a name="requirements"></a><span data-ttu-id="5ca87-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5ca87-120">Requirements</span></span>



| <span data-ttu-id="5ca87-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="5ca87-121">Requirement</span></span> | <span data-ttu-id="5ca87-122">Value</span><span class="sxs-lookup"><span data-stu-id="5ca87-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ca87-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ca87-123">Minimum supported client</span></span><br/> | <span data-ttu-id="5ca87-124">Solo aplicaciones de escritorio de Windows XP Tablet PC Edition \[\]</span><span class="sxs-lookup"><span data-stu-id="5ca87-124">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="5ca87-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5ca87-125">Minimum supported server</span></span><br/> | <span data-ttu-id="5ca87-126">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5ca87-126">None supported</span></span><br/>                                                                                         |
| <span data-ttu-id="5ca87-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="5ca87-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="5ca87-128"><dt>Journal. h (también requiere Journal \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="5ca87-128"><dt>Journal.h (also requires journal\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="5ca87-129">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5ca87-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ca87-130"><dt>Journal.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ca87-130"><dt>Journal.dll</dt></span></span> </dl>                            |



## <a name="see-also"></a><span data-ttu-id="5ca87-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="5ca87-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ca87-132">**Interfaz IJournalReader**</span><span class="sxs-lookup"><span data-stu-id="5ca87-132">**IJournalReader Interface**</span></span>](ijournalreader.md)
</dt> <dt>

[<span data-ttu-id="5ca87-133">Referencia del esquema del lector de Journal</span><span class="sxs-lookup"><span data-stu-id="5ca87-133">Journal Reader Schema Reference</span></span>](journal-reader-schema-reference.md)
</dt> </dl>

 

