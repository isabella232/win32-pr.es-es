---
title: IWMPNetwork setProxyExceptionList, método
description: El método setProxyExceptionList especifica la lista de excepciones de proxy. | IWMPNetwork setProxyExceptionList, método
ms.assetid: a7a5e9ad-f71f-431e-9a53-b56456778104
keywords:
- método setProxyExceptionList de Windows Media Player
- método setProxyExceptionList Windows Media Player, interfaz IWMPNetwork
- Interfaz IWMPNetwork Windows Media Player, método setProxyExceptionList
topic_type:
- apiref
api_name:
- IWMPNetwork.setProxyExceptionList
api_location:
- Interop.WMPLib.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5dad011dee8e1199e6111be60acfec41d85d1e58
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691106"
---
# <a name="iwmpnetworksetproxyexceptionlist-method"></a><span data-ttu-id="35168-107">IWMPNetwork:: setProxyExceptionList (método)</span><span class="sxs-lookup"><span data-stu-id="35168-107">IWMPNetwork::setProxyExceptionList method</span></span>

<span data-ttu-id="35168-108">El método **setProxyExceptionList** especifica la lista de excepciones de proxy.</span><span class="sxs-lookup"><span data-stu-id="35168-108">The **setProxyExceptionList** method specifies the proxy exception list.</span></span>

## <a name="syntax"></a><span data-ttu-id="35168-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35168-109">Syntax</span></span>


```CSharp
public void setProxyExceptionList(
  System.String bstrProtocol,
  System.String pbstrExceptionList
);
```


```VB

Public Sub setProxyExceptionList( _
  ByVal bstrProtocol As System.String, _
  ByVal pbstrExceptionList As System.String _
)
Implements IWMPNetwork.setProxyExceptionList
```





## <a name="parameters"></a><span data-ttu-id="35168-110">Parámetros</span><span class="sxs-lookup"><span data-stu-id="35168-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35168-111">*bstrProtocol* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="35168-111">*bstrProtocol* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35168-112">**System. String** que es el nombre del protocolo.</span><span class="sxs-lookup"><span data-stu-id="35168-112">A **System.String** that is the protocol name.</span></span> <span data-ttu-id="35168-113">Para obtener una lista de protocolos admitidos, consulte [protocolos y tipos de archivo admitidos](supported-protocols-and-file-types.md).</span><span class="sxs-lookup"><span data-stu-id="35168-113">For a list of supported protocols, see [Supported Protocols and File Types](supported-protocols-and-file-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="35168-114">*pbstrExceptionList* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="35168-114">*pbstrExceptionList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="35168-115">**System. String** que es una lista de hosts delimitados por punto y coma para los que se omite el servidor proxy.</span><span class="sxs-lookup"><span data-stu-id="35168-115">A **System.String** that is a semicolon-delimited list of hosts for which the proxy server is bypassed.</span></span> <span data-ttu-id="35168-116">Los espacios iniciales y finales no deben estar presentes.</span><span class="sxs-lookup"><span data-stu-id="35168-116">Leading and trailing spaces should not be present.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35168-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35168-117">Return value</span></span>

<span data-ttu-id="35168-118">Este método no devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="35168-118">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="35168-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="35168-119">Remarks</span></span>

<span data-ttu-id="35168-120">Esta es una lista de equipos, dominios y/o direcciones que omitirán el servidor proxy cuando la parte del host de la dirección URL de destino coincida con una entrada de la lista.</span><span class="sxs-lookup"><span data-stu-id="35168-120">This is a list of computers, domains, and/or addresses that will bypass the proxy server when the host portion of the target URL matches an entry in the list.</span></span>

<span data-ttu-id="35168-121">El \* carácter se puede usar como carácter comodín para enumerar entradas.</span><span class="sxs-lookup"><span data-stu-id="35168-121">The \* character can be used as a wildcard character for listing entries.</span></span> <span data-ttu-id="35168-122">Por ejemplo, \* . com coincidiría con todos los hosts del dominio com, mientras \* que 67. coincidiría con todos los hosts de la clase 67 A la subred.</span><span class="sxs-lookup"><span data-stu-id="35168-122">For example, \*.com would match all hosts in the com domain, while 67.\* would match all hosts in the 67 class A subnet.</span></span>

<span data-ttu-id="35168-123">Este método no tiene ningún efecto a menos que el valor recuperado de **IWMPNetwork. getProxySettings** es 2 (use la configuración manual).</span><span class="sxs-lookup"><span data-stu-id="35168-123">This method has no effect unless the value retrieved from **IWMPNetwork.getProxySettings** is 2 (use manual settings).</span></span>

<span data-ttu-id="35168-124">Este método produce un error a menos que la aplicación que realiza la llamada se ejecute en el equipo local o en la intranet.</span><span class="sxs-lookup"><span data-stu-id="35168-124">This method fails unless the calling application is running on the local computer or intranet.</span></span>

## <a name="examples"></a><span data-ttu-id="35168-125">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="35168-125">Examples</span></span>

<span data-ttu-id="35168-126">En el ejemplo de código siguiente se usa **setProxyExceptionList** para especificar una lista de hosts para los que se omite el servidor proxy cuando se usa el protocolo MMS.</span><span class="sxs-lookup"><span data-stu-id="35168-126">The following code example uses **setProxyExceptionList** to specify a list of hosts for which the proxy server is bypassed when using the MMS protocol.</span></span> <span data-ttu-id="35168-127">La nueva lista se recupera de un cuadro de texto cuando se hace clic en un botón.</span><span class="sxs-lookup"><span data-stu-id="35168-127">The new list is retrieved from a text box when a button is clicked.</span></span> <span data-ttu-id="35168-128">El objeto **AxWMPLib. AxWindowsMediaPlayer** se representa mediante la variable denominada Player.</span><span class="sxs-lookup"><span data-stu-id="35168-128">The **AxWMPLib.AxWindowsMediaPlayer** object is represented by the variable named player.</span></span>


```CSharp
private void setExList_Click(object sender, System.EventArgs e)
{
    // Test whether proxy settings are manual.
    if (player.network.getProxySettings("MMS") == 2)
    {
        // Store the user's new exception list.
        string proxyxlist = exListText.Text;

        // Set the exception list.
        player.network.setProxyExceptionList("MMS", proxyxlist);
    }
    else
    {
        // Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show("Proxy settings must be manual!");
    }
}
```


```VB

Public Sub setExList_Click(ByVal sender As Object, ByVal e As System.EventArgs) Handles setExList.Click

    &#39; Test whether proxy settings are manual.
    If (player.network.getProxySettings(&quot;MMS&quot;) = 2) Then

        &#39; Store the user&#39;s new exception list.
        Dim proxyxlist As String = exListText.Text

        &#39; Set the exception list.
        player.network.setProxyExceptionList(&quot;MMS&quot;, proxyxlist)

    Else

        &#39; Warn that the proxy settings must be set to 2 (manual).
        System.Windows.Forms.MessageBox.Show(&quot;Proxy settings must be manual!&quot;)

    End If

End Sub
```





## <a name="requirements"></a><span data-ttu-id="35168-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35168-129">Requirements</span></span>



| <span data-ttu-id="35168-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="35168-130">Requirement</span></span> | <span data-ttu-id="35168-131">Value</span><span class="sxs-lookup"><span data-stu-id="35168-131">Value</span></span> |
|----------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35168-132">Versión</span><span class="sxs-lookup"><span data-stu-id="35168-132">Version</span></span><br/>   | <span data-ttu-id="35168-133">Windows Media Player 9 series o posterior</span><span class="sxs-lookup"><span data-stu-id="35168-133">Windows Media Player 9 Series or later</span></span><br/>                                                                      |
| <span data-ttu-id="35168-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="35168-134">Namespace</span></span><br/> | <span data-ttu-id="35168-135">**WMPLib**</span><span class="sxs-lookup"><span data-stu-id="35168-135">**WMPLib**</span></span><br/>                                                                                                  |
| <span data-ttu-id="35168-136">Ensamblado</span><span class="sxs-lookup"><span data-stu-id="35168-136">Assembly</span></span><br/>  | <dl> <span data-ttu-id="35168-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span><span class="sxs-lookup"><span data-stu-id="35168-137"><dt>Interop.WMPLib.dll (Interop.WMPLib.dll.dll)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35168-138">Vea también</span><span class="sxs-lookup"><span data-stu-id="35168-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35168-139">**Interfaz IWMPNetwork (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="35168-139">**IWMPNetwork Interface (VB and C#)**</span></span>](iwmpnetwork--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="35168-140">**IWMPNetwork. getProxyExceptionList (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="35168-140">**IWMPNetwork.getProxyExceptionList (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxyexceptionlist--vb-and-c.md)
</dt> <dt>

[<span data-ttu-id="35168-141">**IWMPNetwork. getProxySettings (VB y C#)**</span><span class="sxs-lookup"><span data-stu-id="35168-141">**IWMPNetwork.getProxySettings (VB and C#)**</span></span>](wmplibiwmpnetwork-iwmpnetwork-getproxysettings--vb-and-c.md)
</dt> </dl>

 

 





