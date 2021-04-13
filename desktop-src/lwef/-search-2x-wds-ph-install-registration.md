---
title: Instalar y registrar controladores de protocolo (características heredadas del entorno de Windows)
description: La instalación de controladores de protocolo implica copiar los archivos DLL en una ubicación adecuada en el directorio de archivos de programa y registrarlos.
ms.assetid: 3da32de1-2dc4-46d3-80d0-cc45a36f12f9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec07f96a92b04fb489aeeb76b705efb81b5754f0
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104359651"
---
# <a name="installing-and-registering-protocol-handlers-legacy-windows-environment-features"></a><span data-ttu-id="8be9d-103">Instalar y registrar controladores de protocolo (características heredadas del entorno de Windows)</span><span class="sxs-lookup"><span data-stu-id="8be9d-103">Installing and Registering Protocol Handlers (Legacy Windows Environment Features)</span></span>

> [!NOTE]
> <span data-ttu-id="8be9d-104">Windows Desktop Search 2. x es una tecnología obsoleta que estaba disponible originalmente como complemento para Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8be9d-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="8be9d-105">En versiones posteriores, use la [búsqueda de Windows](../search/-search-3x-wds-overview.md) en su lugar.</span><span class="sxs-lookup"><span data-stu-id="8be9d-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="8be9d-106">La instalación de **controladores de protocolo** implica copiar los archivos dll en una ubicación adecuada en el directorio de archivos de programa y registrarlos.</span><span class="sxs-lookup"><span data-stu-id="8be9d-106">Installing **protocol handlers** involves copying the DLL(s) to an appropriate location in the Program Files directory and registering them.</span></span>

<span data-ttu-id="8be9d-107">Esta sección contiene los siguientes temas:</span><span class="sxs-lookup"><span data-stu-id="8be9d-107">This section contains the following topics:</span></span>

-   [<span data-ttu-id="8be9d-108">Instrucciones de instalación</span><span class="sxs-lookup"><span data-stu-id="8be9d-108">Installation Guidelines</span></span>](#installation-guidelines)
-   [<span data-ttu-id="8be9d-109">Para registrar los controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="8be9d-109">To Register Protocol Handlers</span></span>](#to-register-protocol-handlers)
-   [<span data-ttu-id="8be9d-110">Para registrar extensiones de Shell</span><span class="sxs-lookup"><span data-stu-id="8be9d-110">To Register Shell Extensions</span></span>](#to-register-shell-extensions)

## <a name="installation-guidelines"></a><span data-ttu-id="8be9d-111">Instrucciones de instalación</span><span class="sxs-lookup"><span data-stu-id="8be9d-111">Installation Guidelines</span></span>

<span data-ttu-id="8be9d-112">Los controladores de protocolo deben implementar el registro automático para la instalación y deben seguir estas directrices:</span><span class="sxs-lookup"><span data-stu-id="8be9d-112">Protocol handlers should implement self-registration for installation and should follow these guidelines:</span></span>

-   <span data-ttu-id="8be9d-113">El instalador debe utilizar el instalador EXE o MSI.</span><span class="sxs-lookup"><span data-stu-id="8be9d-113">The installer must use either EXE or MSI installer.</span></span>
-   <span data-ttu-id="8be9d-114">Se deben proporcionar las notas de la versión.</span><span class="sxs-lookup"><span data-stu-id="8be9d-114">Release notes must be provided.</span></span>
-   <span data-ttu-id="8be9d-115">Se debe crear una entrada **Agregar o quitar programas** para cada complemento instalado.</span><span class="sxs-lookup"><span data-stu-id="8be9d-115">An **Add/Remove Programs** entry must be created for each add-in installed.</span></span>
-   <span data-ttu-id="8be9d-116">El instalador debe asumir toda la configuración del registro para el tipo de archivo o almacén concreto que el complemento actual entienda.</span><span class="sxs-lookup"><span data-stu-id="8be9d-116">The installer must take over all registry settings for the particular file type or store that the current add-in understands.</span></span>
-   <span data-ttu-id="8be9d-117">Si se está sobrescribiendo un complemento anterior, el instalador debe notificar al usuario.</span><span class="sxs-lookup"><span data-stu-id="8be9d-117">If a previous add-in is being overwritten, the installer should notify the user.</span></span>
-   <span data-ttu-id="8be9d-118">Si un complemento más reciente ha sobrescrito el complemento anterior, debería tener la capacidad de restaurar la funcionalidad del complemento anterior y convertirlo de nuevo en el complemento predeterminado para ese tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="8be9d-118">If a newer add-in has overwritten the previous add-in, there should be the ability to restore the previous add-in's functionality and make it the default add-in for that file type again.</span></span>

## <a name="to-register-protocol-handlers"></a><span data-ttu-id="8be9d-119">Para registrar los controladores de protocolo</span><span class="sxs-lookup"><span data-stu-id="8be9d-119">To Register Protocol Handlers</span></span>

<span data-ttu-id="8be9d-120">Debe hacer 14 entradas en el registro para registrar el componente de controlador de protocolo, donde:</span><span class="sxs-lookup"><span data-stu-id="8be9d-120">You need to make fourteen entries in the registry to register the protocol handler component, where:</span></span>

-   <span data-ttu-id="8be9d-121">*Ver \_ Ind \_ ProgID* es el ProgID independiente de la versión de la implementación del controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="8be9d-121">*Ver\_Ind\_ProgID* is the version independent ProgID of the protocol handler implementation</span></span>
-   <span data-ttu-id="8be9d-122">*Ver \_ \_Identificador de programa (ProgID* ) de DEP es el ProgID dependiente de la versión de la implementación del controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="8be9d-122">*Ver\_Dep\_ProgID* is the version dependent ProgID of the protocol handler implementation</span></span>
-   <span data-ttu-id="8be9d-123">*CLSID \_ 1* es el CLSID de la implementación del controlador de protocolo</span><span class="sxs-lookup"><span data-stu-id="8be9d-123">*CLSID\_1* is the CLSID of the protocol handler implementation</span></span>

1.  <span data-ttu-id="8be9d-124">Registre el ProgID independiente de la versión con las claves y los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="8be9d-124">Register the version independent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Ind_ProgID>/CurVer
       (Default) = <Ver_Dep_ProgID>
    ```

2.  <span data-ttu-id="8be9d-125">Registre el ProgID dependiente de la versión con los siguientes valores y claves:</span><span class="sxs-lookup"><span data-stu-id="8be9d-125">Register the version dependent ProgID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\<Ver_Dep_ProgID>/CLSID
       (Default) = {CLSID_1}
    ```

3.  <span data-ttu-id="8be9d-126">Registre el CLSID del controlador de protocolo con las claves y los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="8be9d-126">Register the protocol handler's CLSID with the following keys and values:</span></span>

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}
       (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/InprocServer32
       (Default) = <DLL Install Path>
       Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/ProgID
       (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/ShellFolder
       Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/TypeLib
       (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT\{CLSID_1}/VersionIndependentProgID
       (Default) = <Ver_Ind_ProgID>"
    ```

4.  <span data-ttu-id="8be9d-127">Registre el controlador de protocolo con búsqueda en el escritorio de Windows:</span><span class="sxs-lookup"><span data-stu-id="8be9d-127">Register the protocol handler with Windows Desktop Search:</span></span>

    ```
    HKEY_LOCAL_MACHINE\Software\Microsoft\RSSearch\ProtocolHandlers
       Protocol Name = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER\Software\Microsoft\RSSearch\ProtocolHandlers
       Protocol Name = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER\Software\Microsoft\Windows Desktop Search\DS\Index\ProtocolHandlers\<Protocol Name>
       HasRequirements = dword:00000000
       HasStartPage = dword:00000000
    ```

## <a name="to-register-shell-extensions"></a><span data-ttu-id="8be9d-128">Para registrar extensiones de Shell</span><span class="sxs-lookup"><span data-stu-id="8be9d-128">To Register Shell Extensions</span></span>

<span data-ttu-id="8be9d-129">Debe crear dos entradas en el registro para registrar la extensión de Shell del controlador de protocolo.</span><span class="sxs-lookup"><span data-stu-id="8be9d-129">You need to make two entries in the registry to register the protocol handler's Shell extension.</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Desktop\NameSpace\{CLSID of PH Implementation}
   (Default) = <Shell Implementation Description>
```

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Explorer\Shell Extensions\Approved
   {CLSID of PH Implementation} = <Shell Implementation Description>
```

 

 




