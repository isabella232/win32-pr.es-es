---
description: 'Más información sobre: Métodos DurableCommitCallback'
title: Métodos DurableCommitCallback (Microsoft.Isam.Esent.Interop.Windows8)
TOCTitle: DurableCommitCallback methods
ms:assetid: Methods.T:Microsoft.Isam.Esent.Interop.Windows8.DurableCommitCallback
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.windows8.durablecommitcallback_methods(v=EXCHG.10)
ms:contentKeyID: 55104392
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: 1a337d4e62b0eeeb8c5638430d728da37e8e8dc2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127571816"
---
# <a name="durablecommitcallback-methods"></a>Métodos DurableCommitCallback

Incluir miembros protegidos  
Incluir miembros heredados  

El [tipo DurableCommitCallback](./durablecommitcallback-class.md) expone los miembros siguientes.

## <a name="methods"></a>Métodos

<table>
<thead>
<tr class="header">
<th> </th>
<th>Nombre</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn350541(v=exchg.10).md">CheckObjectIsNotDisposed</a></td>
<td>Produce una excepción si se ha eliminado este objeto. (Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn350553(v=exchg.10).md">Dispose()</a></td>
<td>Elimine este objeto y libere el recurso subyacente de Esent. (Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn350543(v=exchg.10).md">Dispose(Boolean)</a></td>
<td>Llamado por Dispose y el finalizador. (Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn335442(v=exchg.10).md">Fin</a></td>
<td>Finaliza la sesión de confirmación duradera.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn350552(v=exchg.10).md">Finalizar</a></td>
<td>Finalizará una instancia de la clase EsentResource. (Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gethashcode#System_Object_GetHashCode">GetHashCode</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.gettype#System_Object_GetType">Gettype</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn335327(v=exchg.10).md">ReleaseResource</a></td>
<td>Libera la sesión de confirmación duradera. (Invalida <a href="dn350545(v=exchg.10).md">EsentResource.ReleaseResource()</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn350576(v=exchg.10).md">ResourceWasAllocated</a></td>
<td>Lo llama una subclase cuando se asigna un recurso. (Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn350577(v=exchg.10).md">ResourceWasReleased</a></td>
<td>Lo llama una subclase cuando se libera un recurso. (Se hereda de <a href="dn319890(v=exchg.10).md">EsentResource).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn335445(v=exchg.10).md">ToString</a></td>
<td>Genera una representación de cadena de la estructura . (Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>).</td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[DurableCommitCallback (clase)](./durablecommitcallback-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop.Windows8](./microsoft.isam.esent.interop.windows8-namespace.md)
