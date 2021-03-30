---
title: 'Método de carga: CPapFile'
description: Cuando estas operaciones se realizan correctamente, se libera la interfaz IStorage obtenida. Esto cierra el archivo e indica que el archivo no se mantiene abierto durante otras operaciones de cliente. Se volverá a abrir cuando sea necesario.
ms.assetid: 40f79adb-87f3-4b0e-9cfe-927a4bc9ada5
keywords:
- 'Método de carga: CPapFile'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1fe70be7241fe1e1eaeb779317e11a76fb479f76
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903904"
---
# <a name="load-method---cpapfile"></a><span data-ttu-id="8b571-106">Método de carga: CPapFile</span><span class="sxs-lookup"><span data-stu-id="8b571-106">Load Method - CPapFile</span></span>

<span data-ttu-id="8b571-107">Cuando estas operaciones se realizan correctamente, se libera la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) obtenida.</span><span class="sxs-lookup"><span data-stu-id="8b571-107">When these operations are successful, the obtained [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface is released.</span></span> <span data-ttu-id="8b571-108">Esto cierra el archivo e indica que el archivo no se mantiene abierto durante otras operaciones de cliente.</span><span class="sxs-lookup"><span data-stu-id="8b571-108">This closes the file and indicates that the file is not held open during other client operations.</span></span> <span data-ttu-id="8b571-109">Se volverá a abrir cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="8b571-109">It will be reopened when required.</span></span>

<span data-ttu-id="8b571-110">Este ejemplo es el método  **Load** de **CPapFile** de Papfile. cpp.</span><span class="sxs-lookup"><span data-stu-id="8b571-110">This example is the **CPapFile** **Load** method from Papfile.cpp.</span></span>


```C++
HRESULT CPapFile::Load(
                      SHORT nLockKey,
                      TCHAR* pszFileName)
  {
    HRESULT hr = E_FAIL;
    BOOL bNewFile = (NULL != pszFileName);
    TCHAR* pszFile;

    // If null file name passed then use current file name.
    pszFile = bNewFile ? pszFileName : m_szCurFileName;

    // Verify that the file is using the APPUTIL function.
    if (FileExist(pszFile))
    {
      // Use the COM service to verify that the file is actually a 
      // valid compound file.
      hr = StgIsStorageFile(pszFile);
      if (SUCCEEDED(hr))
      {
        // Use the COM service to open the compound file and
        // obtain an IStorage interface.
        hr = StgOpenStorage(
               pszFile,
               NULL,
               STGM_DIRECT | STGM_READ | STGM_SHARE_EXCLUSIVE,
               NULL,
               0,
               &m_pIStorage);
        if (SUCCEEDED(hr))
        {
          // An IStorage interface has been obtained. Now, request 
          // the COPaper object on the server side to load into  
          // itself the file's paper data using IStorage for our 
          // client-provided compound file.
          hr = m_pIPaper->Load(nLockKey, m_pIStorage);
          if (SUCCEEDED(hr))
          {
            // The paper data was loaded and a current compound
            // file name exists. Copy it for later use in a saves 
            // and loads.
            if (bNewFile)
              StringCchCopy(m_szCurFileName, sizeof(m_szCurFileName), pszFileName);
          }

          // The Storage object is not required now. Do not hold the 
          // file open. Re-obtain the IStorage again later, when 
          // required (and thus re-open the compound file) for
          // another save or load.
          RELEASE_INTERFACE(m_pIStorage);
        }
      }
    }

    return (hr);
  }
  
```



### <a name="remarks"></a><span data-ttu-id="8b571-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8b571-111">Remarks</span></span>

<span data-ttu-id="8b571-112">Al igual que con el método [**Save**](save-method---cpapfile.md) , si se pasa **null** para el parámetro *pszFileName* , se usa el contenido almacenado del miembro **m \_ szCurFileName** para el nombre de archivo.</span><span class="sxs-lookup"><span data-stu-id="8b571-112">As with the [**Save**](save-method---cpapfile.md) method, if **NULL** is passed for the *pszFileName* parameter, the stored content of member **m\_szCurFileName** is used for the file name.</span></span> <span data-ttu-id="8b571-113">Dado que se puede abrir un archivo existente, la función APPUTIL **FileExist** se usa en primer lugar para comprobar que el archivo existe.</span><span class="sxs-lookup"><span data-stu-id="8b571-113">Because an existing file may be opened, the APPUTIL **FileExist** function is first used to verify that the file exists.</span></span> <span data-ttu-id="8b571-114">Si existe, se llama a la función estándar del servicio [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) para comprobar el formato del archivo y determinar si es un archivo compuesto válido.</span><span class="sxs-lookup"><span data-stu-id="8b571-114">If it exists, the standard [**StgIsStorageFile**](/windows/desktop/api/coml2api/nf-coml2api-stgisstoragefile) service function is called to verify the format of the file to determine if it is a valid compound file.</span></span>

<span data-ttu-id="8b571-115">Si el archivo es válido, se llama a la función de servicio [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) estándar para abrir el archivo y devolver un puntero a una interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) para él.</span><span class="sxs-lookup"><span data-stu-id="8b571-115">If the file is valid, the standard [**StgOpenStorage**](/windows/desktop/api/coml2api/nf-coml2api-stgopenstorage) service function is called to open the file and return a pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface for it.</span></span>

<span data-ttu-id="8b571-116">El primer parámetro es el nombre del archivo compuesto que se va a abrir.</span><span class="sxs-lookup"><span data-stu-id="8b571-116">The first parameter is the name of the compound file to open.</span></span> <span data-ttu-id="8b571-117">Al igual que con la llamada a [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) , esta cadena se espera en el formato Unicode y durante la compilación ANSI se usa una macro APPUTIL para asegurarse de que el parámetro ANSI se convierte en el Unicode esperado.</span><span class="sxs-lookup"><span data-stu-id="8b571-117">As with the [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile) call, this string is expected in the Unicode form, and during ANSI compilation an APPUTIL macro is used to ensure the ANSI parameter is converted to the expected Unicode.</span></span>

<span data-ttu-id="8b571-118">El segundo parámetro de almacenamiento de prioridad es **null**, lo que indica que no se utiliza en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8b571-118">The second priority storage parameter is **NULL**, indicating it is not used in this sample.</span></span>

<span data-ttu-id="8b571-119">Las marcas de modo de acceso se pasan como el tercer parámetro para especificar qué modos de acceso se permiten en el archivo abierto.</span><span class="sxs-lookup"><span data-stu-id="8b571-119">The access mode flags are passed as the third parameter to specify what access modes are permitted on the opened file.</span></span> <span data-ttu-id="8b571-120">[**STGM \_ LEER**](stgm-constants.md) abre el archivo con permiso de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="8b571-120">[**STGM\_READ**](stgm-constants.md) opens the file with read-only permission.</span></span> <span data-ttu-id="8b571-121">[**STGM \_ DIRECT**](stgm-constants.md) abre el archivo para el acceso directo, en lugar del acceso con transacciones.</span><span class="sxs-lookup"><span data-stu-id="8b571-121">[**STGM\_DIRECT**](stgm-constants.md) opens the file for direct access, as opposed to transacted access.</span></span> <span data-ttu-id="8b571-122">[**STGM \_ Recurso compartido \_ exclusivo**](stgm-constants.md) abre el archivo para uso exclusivo y no compartido por parte del autor de la llamada.</span><span class="sxs-lookup"><span data-stu-id="8b571-122">[**STGM\_SHARE\_EXCLUSIVE**](stgm-constants.md) opens the file for exclusive, non-shared use by the caller.</span></span>

<span data-ttu-id="8b571-123">El cuarto parámetro de exclusión de elemento en **null**, que indica que no se utiliza en este ejemplo.</span><span class="sxs-lookup"><span data-stu-id="8b571-123">The fourth element exclusion parameter in **NULL**, indicating it is not used in this sample.</span></span>

<span data-ttu-id="8b571-124">El quinto parámetro está reservado para un uso futuro y debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="8b571-124">The fifth parameter is reserved for future use and must be zero.</span></span>

<span data-ttu-id="8b571-125">La dirección de la variable de puntero **m \_ pIStorage** se pasa como el sexto parámetro.</span><span class="sxs-lookup"><span data-stu-id="8b571-125">The address of pointer variable **m\_pIStorage** is passed as the sixth parameter.</span></span> <span data-ttu-id="8b571-126">Cuando la llamada devuelve correctamente, **m \_ pIStorage** contiene un puntero a una interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) .</span><span class="sxs-lookup"><span data-stu-id="8b571-126">When the call successfully returns, **m\_pIStorage** contains a pointer to an [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface.</span></span> <span data-ttu-id="8b571-127">Esta es la interfaz que se utiliza para las operaciones posteriores en el archivo abierto.</span><span class="sxs-lookup"><span data-stu-id="8b571-127">This is the interface that is used for any subsequent operations on the opened file.</span></span>

<span data-ttu-id="8b571-128">La operación importante en este caso es que el objeto de copapeles cargue sus datos de dibujo del archivo.</span><span class="sxs-lookup"><span data-stu-id="8b571-128">The important operation in this case is to have the COPaper object load its drawing data from the file.</span></span> <span data-ttu-id="8b571-129">Para ello, se usa el método **Load** de la interfaz [**IPaper**](ipaper-methods.md) del copaper.</span><span class="sxs-lookup"><span data-stu-id="8b571-129">This is done above using the **Load** method of COPaper's [**IPaper**](ipaper-methods.md) interface.</span></span> <span data-ttu-id="8b571-130">Si el copapel se ejecuta correctamente al cargar sus datos mediante el [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) proporcionado, el nombre del archivo compuesto se copia en **m \_ szCurFileName** como el nuevo nombre de archivo actual.</span><span class="sxs-lookup"><span data-stu-id="8b571-130">If COPaper succeeds in loading its data using the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) provided, the name of the compound file is copied into **m\_szCurFileName** as the new current file name.</span></span>

<span data-ttu-id="8b571-131">Cuando estas operaciones se completan correctamente, se libera la interfaz [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) obtenida.</span><span class="sxs-lookup"><span data-stu-id="8b571-131">When these operations are successfully completed, the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface that was obtained is released.</span></span> <span data-ttu-id="8b571-132">Esto cierra el archivo y significa que el archivo no se mantiene abierto durante otras operaciones de cliente.</span><span class="sxs-lookup"><span data-stu-id="8b571-132">This closes the file and means that the file is not held open during other client operations.</span></span> <span data-ttu-id="8b571-133">Se volverá a abrir cuando sea necesario.</span><span class="sxs-lookup"><span data-stu-id="8b571-133">It will be reopened when required.</span></span>

 

 




