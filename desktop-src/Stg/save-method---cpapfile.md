---
title: 'Método Save: CPapFile'
description: Cuando se inicializa CPapFile, se puede usar para guardar los datos de dibujo actuales contenidos en el objeto de copaper.
ms.assetid: ceac32e5-7d47-480b-b1cd-5a17ac04dd0c
keywords:
- 'Método Save: CPapFile'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3166b649f28cb1a8ddc37e9efc53465a6cb5d3e0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103994606"
---
# <a name="save-method---cpapfile"></a><span data-ttu-id="523c2-104">Método Save: CPapFile</span><span class="sxs-lookup"><span data-stu-id="523c2-104">Save Method - CPapFile</span></span>

<span data-ttu-id="523c2-105">Cuando se inicializa **CPapFile** , se puede usar para guardar los datos de dibujo actuales contenidos en el objeto de copaper.</span><span class="sxs-lookup"><span data-stu-id="523c2-105">When **CPapFile** is initialized, it can be used to save the current drawing data held in the COPaper object.</span></span>

## <a name="save-method-papfilecpp"></a><span data-ttu-id="523c2-106">Método Save (PAPFILE. CPP</span><span class="sxs-lookup"><span data-stu-id="523c2-106">Save Method (PAPFILE.CPP)</span></span>

<span data-ttu-id="523c2-107">Este ejemplo es el método  [**Save**](ipaper--save.md) de **CPapFile** de Papfile. cpp.</span><span class="sxs-lookup"><span data-stu-id="523c2-107">This example is the **CPapFile** [**Save**](ipaper--save.md) method from Papfile.cpp.</span></span>


```C++
HRESULT CPapFile::Save(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If a null file name is passed, then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Use the COM service to reopen, or create, the compound file.
    hr = StgCreateDocfile(
        pszFile,
    STGM_CREATE | STGM_DIRECT | STGM_READWRITE | STGM_SHARE_EXCLUSIVE,
        0,
        &m_pIStorage);
    if (SUCCEEDED(hr))
    {
      // Obtained the IStorage. The compound file is open.
      // Instruct the COPaper object on the server side to save its
      // paper data into the compound file using the IStorage of our
      // client-provided compound file.
      hr = m_pIPaper->Save(nLockKey, m_pIStorage);
      if (SUCCEEDED(hr))
      {
        // The paper data was saved and obtained a new current 
        // compound file name. Copy it for later use in saves 
        // and loads.
        if (bNewFile)
          StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
      }

      // Storage complete. Do not hold the file open.
      // Re-obtain the IStorage again later (and thus re-open
      // the compound file) when required for another save or load.
      RELEASE_INTERFACE(m_pIStorage);
    }

    return (hr);
  }
  
```



<span data-ttu-id="523c2-108">Si se pasa **null** para el parámetro *pszFileName* , se usa el contenido almacenado del miembro **m \_ szCurFileName** para el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="523c2-108">If **NULL** is passed for the *pszFileName* parameter, the stored content of member **m\_szCurFileName** is used for the file name.</span></span> <span data-ttu-id="523c2-109">*NLockKey* es la clave de bloqueo de cliente obtenida en una llamada anterior al método de [**bloqueo**](ipaper-methods.md) de copapeles en la interfaz **IPaper** .</span><span class="sxs-lookup"><span data-stu-id="523c2-109">The *nLockKey* is the client lock key obtained in a previous call to the COPaper [**Lock**](ipaper-methods.md) method in the **IPaper** interface.</span></span>

<span data-ttu-id="523c2-110">Se llama a la función de servicio [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) estándar com para crear el archivo compuesto en el que se guardarán los datos del dibujo.</span><span class="sxs-lookup"><span data-stu-id="523c2-110">The COM standard [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) service function is called to create the compound file in which the drawing data will be saved.</span></span>

<span data-ttu-id="523c2-111">El nombre del archivo compuesto que se va a crear se pasa como primer parámetro.</span><span class="sxs-lookup"><span data-stu-id="523c2-111">The name of the compound file to create is passed as the first parameter.</span></span> <span data-ttu-id="523c2-112">Esto lo espera [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) como una cadena Unicode.</span><span class="sxs-lookup"><span data-stu-id="523c2-112">This is expected by [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) as a Unicode string.</span></span> <span data-ttu-id="523c2-113">Cuando se compila **StoClien** para cadenas ANSI (no se define Unicode, que es el valor predeterminado en el archivo make), esta llamada se reduce realmente a una llamada a una función APPUTIL interna, **\_ StgCreateDocfile**.</span><span class="sxs-lookup"><span data-stu-id="523c2-113">When **StoClien** is compiled for ANSI strings (UNICODE is not defined, which is the default in the makefile), this call actually reduces to a call to an internal APPUTIL function, **A\_StgCreateDocfile**.</span></span> <span data-ttu-id="523c2-114">Esta función realiza la conversión adecuada del parámetro pszFile de ANSI a una versión de Unicode antes de llamar a **StgCreateDocfile**.</span><span class="sxs-lookup"><span data-stu-id="523c2-114">This function performs the proper conversion of the ANSI pszFile parameter to a Unicode version before calling **StgCreateDocfile**.</span></span> <span data-ttu-id="523c2-115">Para obtener más información, vea apputil. h y Stoserve.htm.</span><span class="sxs-lookup"><span data-stu-id="523c2-115">For more information, see Apputil.h and Stoserve.htm.</span></span>

<span data-ttu-id="523c2-116">Las marcas de modo de acceso se pasan como el segundo parámetro y determinan qué modos de acceso se permiten en el nuevo archivo.</span><span class="sxs-lookup"><span data-stu-id="523c2-116">The access mode flags are passed as the second parameter and determine which access modes are permitted on the new file.</span></span> <span data-ttu-id="523c2-117">La marca [STGM \_ Create](stgm-constants.md) Access Mode crea un nuevo archivo compuesto o sobrescribe uno existente del mismo nombre.</span><span class="sxs-lookup"><span data-stu-id="523c2-117">The [STGM\_CREATE](stgm-constants.md) access mode flag creates a new compound file or overwrites an existing one of the same name.</span></span> <span data-ttu-id="523c2-118">[STGM \_ READWRITE](stgm-constants.md) abre el archivo con permiso de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="523c2-118">[STGM\_READWRITE](stgm-constants.md) opens the file with read-write permission.</span></span> <span data-ttu-id="523c2-119">[STGM \_ DIRECT](stgm-constants.md) abre el archivo para el acceso directo, en lugar del acceso con transacciones.</span><span class="sxs-lookup"><span data-stu-id="523c2-119">[STGM\_DIRECT](stgm-constants.md) opens the file for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="523c2-120">[STGM \_ Recurso compartido \_ exclusivo](stgm-constants.md) abre el archivo para uso exclusivo y no compartido por parte del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="523c2-120">[STGM\_SHARE\_EXCLUSIVE](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="523c2-121">El tercer parámetro está reservado y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="523c2-121">The third parameter is reserved and must be zero.</span></span>

<span data-ttu-id="523c2-122">La dirección de la variable de puntero **m \_ pIStorage** se pasa a [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) como el cuarto parámetro.</span><span class="sxs-lookup"><span data-stu-id="523c2-122">The address of pointer variable **m\_pIStorage** is passed to [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) as the fourth parameter.</span></span> <span data-ttu-id="523c2-123">Cuando la llamada devuelve correctamente, **m \_ pIStorage** contiene un puntero de interfaz a una interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="523c2-123">When the call successfully returns, **m\_pIStorage** contains an interface pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="523c2-124">Esta es la interfaz que se utiliza para las operaciones posteriores en el archivo.</span><span class="sxs-lookup"><span data-stu-id="523c2-124">This is the interface that is used for any subsequent operations on the file.</span></span>

<span data-ttu-id="523c2-125">La operación importante en este caso es que el objeto de copapeles almacene sus datos de dibujo en el archivo.</span><span class="sxs-lookup"><span data-stu-id="523c2-125">The important operation in this case is to have the COPaper object store its drawing data in the file.</span></span> <span data-ttu-id="523c2-126">Para ello, use el método [**Save**](ipaper--save.md) de la interfaz [**IPaper**](ipaper-methods.md) de copaper.</span><span class="sxs-lookup"><span data-stu-id="523c2-126">This is done above using the [**Save**](ipaper--save.md) method of the COPaper [**IPaper**](ipaper-methods.md) interface.</span></span> <span data-ttu-id="523c2-127">Si el copapel es correcto al guardar sus datos en el objeto de almacenamiento proporcionado, el nombre del archivo compuesto se copia en **m \_ szCurFileName** como el nuevo nombre de archivo actual.</span><span class="sxs-lookup"><span data-stu-id="523c2-127">If COPaper succeeds in saving its data in the storage object provided, the name of the compound file is copied into **m\_szCurFileName** as the new current file name.</span></span>

 

 




