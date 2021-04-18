---
title: IPaper guardar
description: El foco principal en este código de ejemplo es cómo puede cargar el copaper y guardar sus datos de papel en archivos compuestos. Las implementaciones de los métodos IPaper, Load y Save se describen en detalle.
ms.assetid: 62154658-ff47-425f-94da-ee2806de5318
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96ea49f194e64ab3f0cfd78569b1e6ff9ddee577
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665713"
---
# <a name="ipapersave"></a><span data-ttu-id="88425-104">IPaper:: Save</span><span class="sxs-lookup"><span data-stu-id="88425-104">IPaper::Save</span></span>

<span data-ttu-id="88425-105">El foco principal en este código de ejemplo es cómo puede cargar el copaper y guardar sus datos de papel en archivos compuestos.</span><span class="sxs-lookup"><span data-stu-id="88425-105">The principal focus in this sample code is how COPaper can load and save its paper data in compound files.</span></span> <span data-ttu-id="88425-106">Las implementaciones de los métodos [**IPaper**](ipaper-methods.md), [**Load**](ipaper--load.md)y **Save** se describen en detalle.</span><span class="sxs-lookup"><span data-stu-id="88425-106">The [**IPaper**](ipaper-methods.md), [**Load**](ipaper--load.md), and **Save** method implementations are discussed in detail.</span></span>

<span data-ttu-id="88425-107">A continuación se explica el método **IPaper:: Save** de Paper. cpp.</span><span class="sxs-lookup"><span data-stu-id="88425-107">The following is the **IPaper::Save** method from Paper.cpp.</span></span>


```C++
STDMETHODIMP COPaper::CImpIPaper::Save(
                 SHORT nLockKey,
                 IStorage* pIStorage)
  {
    HRESULT hr = E_FAIL;
    IStream* pIStream;
    ULONG ulToWrite, ulWritten;

    if (OwnThis())
    {
      if (m_bLocked && m_cLockKey == nLockKey && NULL != pIStorage)
      {
        // Use the COM service to mark this compound file as one 
        // that is handled by our server component, DllPaper.
        WriteClassStg(pIStorage, CLSID_DllPaper);

        // Use the COM Service to write user-readable clipboard 
        // format into the compound file.
        WriteFmtUserTypeStg(pIStorage, m_ClipBdFmt, 
                            TEXT(CLIPBDFMT_STR));

        // Create the stream to be used for the actual paper data.
        // Call it "PAPERDATA".
        hr = pIStorage->CreateStream(
               STREAM_PAPERDATA_USTR,
        STGM_CREATE | STGM_WRITE | STGM_DIRECT | STGM_SHARE_EXCLUSIVE,
               0,
               0,
               &pIStream);
        if (SUCCEEDED(hr))
        {
          // Obtained a stream. Write data to it.
          // First, write PAPER_PROPERTIES structure.
          m_PaperProperties.lInkArraySize = m_lInkDataEnd+1;
          m_PaperProperties.crWinColor = m_crWinColor;
          m_PaperProperties.WinRect.right = m_WinRect.right;
          m_PaperProperties.WinRect.bottom = m_WinRect.bottom;
          ulToWrite = sizeof(PAPER_PROPERTIES);
          hr = pIStream->Write(&m_Paper_Properties, ulToWrite, 
                               &ulWritten);
          if (SUCCEEDED(hr) && ulToWrite != ulWritten)
            hr = STG_E_CANTSAVE;
          if (SUCCEEDED(hr))
          {
            // Now, write the complete array of Ink Data.
            ulToWrite = m_PaperProperties.lInkArraySize * 
                                                     sizeof(INKDATA);
            hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
            if (SUCCEEDED(hr) && ulToWrite != ulWritten)
              hr = STG_E_CANTSAVE;
          }

          // Release the stream.
          pIStream->Release();
        }
      }

      UnOwnThis();
    }

    // Notify all other connected clients that Paper is now saved.
    if (SUCCEEDED(hr))
      m_pBackObj->NotifySinks(PAPER_EVENT_SAVED, 0, 0, 0, 0);

    return hr;
  }
```



<span data-ttu-id="88425-108">En esta relación entre cliente y servidor, el copaper no crea el archivo compuesto que se usa para almacenar los datos del papel.</span><span class="sxs-lookup"><span data-stu-id="88425-108">In this client and server relationship, COPaper does not create the compound file used to store paper data.</span></span> <span data-ttu-id="88425-109">En el caso de los métodos **Save** y [**Load**](ipaper--load.md) , el cliente pasa un puntero de interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para un archivo compuesto existente.</span><span class="sxs-lookup"><span data-stu-id="88425-109">For both the **Save** and [**Load**](ipaper--load.md) methods, the client passes an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface pointer for an existing compound file.</span></span> <span data-ttu-id="88425-110">A continuación, usa el **IStorage** para escribir y leer datos en ese archivo compuesto.</span><span class="sxs-lookup"><span data-stu-id="88425-110">It then uses the **IStorage** to write and read data in that compound file.</span></span> <span data-ttu-id="88425-111">En **IPaper:: Save** anterior, se almacenan varios tipos de datos.</span><span class="sxs-lookup"><span data-stu-id="88425-111">In **IPaper::Save** above, several types of data are stored.</span></span>

<span data-ttu-id="88425-112">El CLSID de DllPaper, CLSID \_ DllPaper, se serializa y se almacena en un flujo especial controlado por com en el objeto de almacenamiento llamado " \\ 001CompObj".</span><span class="sxs-lookup"><span data-stu-id="88425-112">The CLSID for DllPaper, CLSID\_DllPaper, is serialized and stored in a special COM-controlled stream within the storage object called "\\001CompObj".</span></span> <span data-ttu-id="88425-113">La función de servicio [**WriteClassStg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) realiza este almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="88425-113">The [**WriteClassStg**](/windows/desktop/api/coml2api/nf-coml2api-writeclassstg) service function performs this storage.</span></span> <span data-ttu-id="88425-114">Estos datos de CLSID almacenados se pueden usar para asociar el contenido de almacenamiento al componente DllPaper que creó y puede interpretarlo.</span><span class="sxs-lookup"><span data-stu-id="88425-114">This stored CLSID data can be used to associate the storage content with the DllPaper component that created and can interpret it.</span></span> <span data-ttu-id="88425-115">En este ejemplo, **StoClien** pasa el almacenamiento raíz y, por tanto, el archivo compuesto completo está asociado al componente DllPaper.</span><span class="sxs-lookup"><span data-stu-id="88425-115">In this sample, the root storage is passed by **StoClien**, and thus the entire compound file is associated with the DllPaper component.</span></span> <span data-ttu-id="88425-116">Estos datos CLSID se pueden recuperar más adelante con una llamada a la función de servicio [**ReadClassStg**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) .</span><span class="sxs-lookup"><span data-stu-id="88425-116">This CLSID data can be retrieved later with a call to the [**ReadClassStg**](/windows/desktop/api/coml2api/nf-coml2api-readclassstg) service function.</span></span>

<span data-ttu-id="88425-117">Dado que DllPaper se encarga de los datos editables, también es adecuado registrar un formato de Portapapeles en el almacenamiento.</span><span class="sxs-lookup"><span data-stu-id="88425-117">Because DllPaper deals with editable data, it is also appropriate to record a clipboard format in the storage.</span></span> <span data-ttu-id="88425-118">Se llama a la función de servicio [**WriteFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) para almacenar una designación de formato del portapapeles y un nombre legible por el usuario para el formato.</span><span class="sxs-lookup"><span data-stu-id="88425-118">The [**WriteFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-writefmtusertypestg) service function is called to store both a clipboard format designation and a user-readable name for the format.</span></span> <span data-ttu-id="88425-119">El nombre legible para el usuario está pensado para la visualización de GUI en listas de selección.</span><span class="sxs-lookup"><span data-stu-id="88425-119">The user-readable name is meant for GUI display in selection lists.</span></span> <span data-ttu-id="88425-120">El nombre pasado usa una macro, CLIPBDFMT \_ Str, que se define como "DllPaper 1,0" en Paper. h.</span><span class="sxs-lookup"><span data-stu-id="88425-120">The name passed above uses a macro, CLIPBDFMT\_STR, which is defined as "DllPaper 1.0" in Paper.h.</span></span> <span data-ttu-id="88425-121">Estos datos almacenados del portapapeles se pueden recuperar más adelante con una llamada a la función de servicio [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg).</span><span class="sxs-lookup"><span data-stu-id="88425-121">This stored clipboard data can be retrieved later with a call to the service function [**ReadFmtUserTypeStg**](/windows/desktop/api/Ole2/nf-ole2-readfmtusertypestg).</span></span> <span data-ttu-id="88425-122">Esta función devuelve un valor de cadena que se asigna mediante el asignador de memoria de la tarea.</span><span class="sxs-lookup"><span data-stu-id="88425-122">This function returns a string value that is allocated using the task memory allocator.</span></span> <span data-ttu-id="88425-123">El autor de la llamada es responsable de liberar la cadena.</span><span class="sxs-lookup"><span data-stu-id="88425-123">The caller is responsible for freeing the string.</span></span>

<span data-ttu-id="88425-124">**Guardar** siguiente crea una secuencia en el almacenamiento para los datos de papel de los papeles.</span><span class="sxs-lookup"><span data-stu-id="88425-124">**Save** next creates a stream in the storage for the COPaper paper data.</span></span> <span data-ttu-id="88425-125">La secuencia se denomina "PAPERDATA" y se pasa mediante la \_ macro Stream PAPERDATA \_ USTR.</span><span class="sxs-lookup"><span data-stu-id="88425-125">The stream is called "PAPERDATA" and is passed using the STREAM\_PAPERDATA\_USTR macro.</span></span> <span data-ttu-id="88425-126">El método [**IStorage:: CreateStream (**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) requiere que esta cadena esté en Unicode.</span><span class="sxs-lookup"><span data-stu-id="88425-126">The [**IStorage::CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) method requires that this string be in Unicode.</span></span> <span data-ttu-id="88425-127">Dado que la cadena se fija en tiempo de compilación, la macro se define como Unicode en Paper. h.</span><span class="sxs-lookup"><span data-stu-id="88425-127">Because the string is fixed at compile time, the macro is defined as Unicode in Paper.h.</span></span>

``` syntax
#define STREAM_PAPERDATA_USTR L"PAPERDATA"
```

<span data-ttu-id="88425-128">La ' L ' antes de la cadena, que indica LONG, logra esto.</span><span class="sxs-lookup"><span data-stu-id="88425-128">The 'L' before the string, indicating LONG, achieves this.</span></span>

<span data-ttu-id="88425-129">El método [**CreateStream (**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) crea y abre una secuencia dentro del almacenamiento especificado.</span><span class="sxs-lookup"><span data-stu-id="88425-129">The [**CreateStream**](/windows/desktop/api/Objidl/nf-objidl-istorage-createstream) method creates and opens a stream within the specified storage.</span></span> <span data-ttu-id="88425-130">Un puntero de interfaz [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) para la nueva secuencia se pasa en una variable de puntero de interfaz de autor de llamada.</span><span class="sxs-lookup"><span data-stu-id="88425-130">An [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface pointer for the new stream is passed in a caller interface pointer variable.</span></span> <span data-ttu-id="88425-131">Se llama a AddRef en este puntero de interfaz dentro de **CreateStream (** y el llamador debe liberar este puntero después de usarlo.</span><span class="sxs-lookup"><span data-stu-id="88425-131">AddRef is called on this interface pointer within **CreateStream**, and the caller must release this pointer after using it.</span></span> <span data-ttu-id="88425-132">El método **CreateStream (** recibe varias marcas de modo de acceso, como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="88425-132">The **CreateStream** method is passed numerous access mode flags, as follows.</span></span>

<span data-ttu-id="88425-133">STGM \_ Create \| STGM \_ Write \| STGM \_ Direct \| STGM \_ share \_</span><span class="sxs-lookup"><span data-stu-id="88425-133">STGM\_CREATE \| STGM\_WRITE \| STGM\_DIRECT \| STGM\_SHARE\_EXCLUSIVE</span></span>

<span data-ttu-id="88425-134">[**STGM \_ CREAR**](stgm-constants.md) crea una nueva secuencia o sobrescribe una existente del mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="88425-134">[**STGM\_CREATE**](stgm-constants.md) creates a new stream or overwrites an existing one of the same name.</span></span> <span data-ttu-id="88425-135">[**STGM \_ ESCRIBIR**](stgm-constants.md) abre el flujo con permiso de escritura.</span><span class="sxs-lookup"><span data-stu-id="88425-135">[**STGM\_WRITE**](stgm-constants.md) opens the stream with write permission.</span></span> <span data-ttu-id="88425-136">[**STGM \_ DIRECT**](stgm-constants.md) abre la secuencia para el acceso directo, en lugar del acceso con transacciones.</span><span class="sxs-lookup"><span data-stu-id="88425-136">[**STGM\_DIRECT**](stgm-constants.md) opens the stream for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="88425-137">[**STGM \_ Recurso compartido \_ exclusivo**](stgm-constants.md) abre el archivo para uso exclusivo y no compartido por parte del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="88425-137">[**STGM\_SHARE\_EXCLUSIVE**](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="88425-138">Una vez creada correctamente la secuencia PAPERDATA, se usa la interfaz [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) para escribir en la secuencia.</span><span class="sxs-lookup"><span data-stu-id="88425-138">After the PAPERDATA stream is successfully created, the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) interface is used to write into the stream.</span></span> <span data-ttu-id="88425-139">El método **IStream:: Write** se usa para almacenar primero el contenido de la estructura de propiedades del papel \_ .</span><span class="sxs-lookup"><span data-stu-id="88425-139">The **IStream::Write** method is used to first store the content of the PAPER\_PROPERTIES structure.</span></span> <span data-ttu-id="88425-140">Es esencialmente un encabezado de propiedades al principio de la secuencia.</span><span class="sxs-lookup"><span data-stu-id="88425-140">This is essentially a properties header at the front of the stream.</span></span> <span data-ttu-id="88425-141">Dado que el número de versión es lo primero en el archivo, se puede leer de forma independiente para determinar cómo tratar los datos que se indican a continuación.</span><span class="sxs-lookup"><span data-stu-id="88425-141">Because the version number is the first thing in the file, it can be read independently to determine how to deal with the data that follows.</span></span> <span data-ttu-id="88425-142">Si la cantidad de datos escritos realmente no es igual a la cantidad solicitada, se anula el método Save y se devuelve STG \_ E \_ CANTSAVE.</span><span class="sxs-lookup"><span data-stu-id="88425-142">If the amount of data actually written does not equal the amount requested, the Save method is aborted, and it returns STG\_E\_CANTSAVE.</span></span>

<span data-ttu-id="88425-143">Guardar toda la matriz de datos de entrada de lápiz en el flujo es sencillo.</span><span class="sxs-lookup"><span data-stu-id="88425-143">Saving the entire array of ink data into the stream is simple.</span></span>


```C++
// Now write the complete array of Ink Data.
  ulToWrite = m_PaperProperties.lInkArraySize * sizeof(INKDATA);
  hr = pIStream->Write(m_paInkData, ulToWrite, &ulWritten);
  if (SUCCEEDED(hr) && ulToWrite != ulWritten)
    hr = STG_E_CANTSAVE;
```



<span data-ttu-id="88425-144">Dado que el método [**IStream:: Write**](/windows/desktop/api/Objidl/nn-objidl-istream) funciona en una matriz de bytes, se calcula el número de bytes de los datos de tinta almacenados en la matriz y la operación de escritura comienza en el inicio de la matriz.</span><span class="sxs-lookup"><span data-stu-id="88425-144">Because the [**IStream::Write**](/windows/desktop/api/Objidl/nn-objidl-istream) method operates on a byte array, the number of bytes of stored ink data in the array is calculated and the write operation begins at the start of the array.</span></span> <span data-ttu-id="88425-145">Si la cantidad de datos escritos realmente no es igual a la cantidad solicitada, el método **Save** devuelve STG \_ E \_ CANTSAVE.</span><span class="sxs-lookup"><span data-stu-id="88425-145">If the amount of data actually written does not equal the amount requested, the **Save** method returns STG\_E\_CANTSAVE.</span></span>

<span data-ttu-id="88425-146">Una vez escrita la secuencia, el método **IPaper:: Save** libera el puntero [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) que estaba usando.</span><span class="sxs-lookup"><span data-stu-id="88425-146">After the stream is written, the **IPaper::Save** method releases the [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream) pointer it was using.</span></span>

<span data-ttu-id="88425-147">El método **Save** también llama al cliente [**IPaperSink**](ipapersink-methods.md) (en el método NotifySinks interno de copaper) para notificar al cliente que se ha completado la operación de guardar.</span><span class="sxs-lookup"><span data-stu-id="88425-147">The **Save** method also calls the client [**IPaperSink**](ipapersink-methods.md) (in the COPaper internal NotifySinks method) to notify the client that the save operation is complete.</span></span> <span data-ttu-id="88425-148">En este momento, el método **Save** vuelve al cliente que realiza la llamada, que normalmente liberará el puntero [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="88425-148">At this point the **Save** method returns to the calling client, which will typically release the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) pointer.</span></span>

 

 




