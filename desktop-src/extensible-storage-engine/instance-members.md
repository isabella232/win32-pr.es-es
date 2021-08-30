---
description: 'Más información sobre: Miembros de instancia'
title: Miembros de instancia
TOCTitle: Instance members
ms:assetid: AllMembers.T:Microsoft.Isam.Esent.Interop.Instance
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instance_members(v=EXCHG.10)
ms:contentKeyID: 55103299
ms.date: 07/30/2014
ms.topic: article
ms.openlocfilehash: f1b3b533c7893385902cad41e1300105995e7b389c61776c47e17341817bbac9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120093865"
---
# <a name="instance-members"></a>Miembros de instancia

Incluir miembros protegidos  
Incluir miembros heredados  

Clase que encapsula un [JET_INSTANCE](./jet-instance-structure.md) en un objeto descartable. La instancia debe cerrarse en último lugar y cerrar la instancia libera todos los demás recursos de la instancia.

El [tipo](./instance-class.md) de instancia expone los miembros siguientes.

## <a name="constructors"></a>Constructores

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn350924(v=exchg.10).md">Instance(String)</a></td>
<td>Inicializa una nueva instancia de la clase Instance. El JET_INSTANCE subyacente se asigna, pero no se inicializa.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn350927(v=exchg.10).md">Instance(String, String)</a></td>
<td>Inicializa una nueva instancia de la clase Instance. El JET_INSTANCE subyacente se asigna, pero no se inicializa.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn350948(v=exchg.10).md">Instance(String, String, TermGrbit)</a></td>
<td>Inicializa una nueva instancia de la clase Instance. El JET_INSTANCE subyacente se asigna, pero no se inicializa.</td>
</tr>
</tbody>
</table>


Superior

## <a name="properties"></a>Propiedades

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
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.isclosed#System_Runtime_InteropServices_SafeHandle_IsClosed">IsClosed</a></td>
<td>(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid.isinvalid#Microsoft_Win32_SafeHandles_SafeHandleZeroOrMinusOneIsInvalid_IsInvalid">IsInvalid</a></td>
<td>(Se hereda de <a href="/dotnet/api/microsoft.win32.safehandles.safehandlezeroorminusoneisinvalid">SafeHandleZeroOrMinusOneIsInvalid).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350941(v=exchg.10).md">JetInstance</a></td>
<td>Obtiene el JET_INSTANCE que contiene esta instancia.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350962(v=exchg.10).md">Parámetros</a></td>
<td>Obtiene instanceParameters para esta instancia.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292128.pubproperty(exchg.10).gif" title="Propiedad pública" alt="Public property" /></td>
<td><a href="dn350964(v=exchg.10).md">TermGrbit</a></td>
<td>Obtiene o establece el TermGrbit de esta instancia.</td>
</tr>
</tbody>
</table>


Superior

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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.close#System_Runtime_InteropServices_SafeHandle_Close">Cerrar</a></td>
<td>(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousaddref#System_Runtime_InteropServices_SafeHandle_DangerousAddRef_System_Boolean__">DangerousAddRef</a></td>
<td>(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousgethandle#System_Runtime_InteropServices_SafeHandle_DangerousGetHandle">DangerousGetHandle</a></td>
<td>(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.dangerousrelease#System_Runtime_InteropServices_SafeHandle_DangerousRelease">DangerousRelease</a></td>
<td>(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose">Dispose()</a></td>
<td>(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.dispose#System_Runtime_InteropServices_SafeHandle_Dispose_System_Boolean_">Dispose(Boolean)</a></td>
<td>(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.object.equals#System_Object_Equals_System_Object_">Es igual a</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.finalize#System_Runtime_InteropServices_SafeHandle_Finalize">Finalizar</a></td>
<td>(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle).</a></td>
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
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn350932(v=exchg.10).md">Init()</a></td>
<td>Inicialice el JET_INSTANCE.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn350954(v=exchg.10).md">Init(InitGrbit)</a></td>
<td>Inicialice el JET_INSTANCE.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn350934(v=exchg.10).md">Init(JET_RSTINFO, InitGrbit)</a></td>
<td>Inicialice el JET_INSTANCE. Esta API requiere al menos la versión vista de ESENT.</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.object.memberwiseclone#System_Object_MemberwiseClone">MemberwiseClone</a></td>
<td>(Se hereda del <a href="/dotnet/api/system.object">objeto</a>).</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="dn350956(v=exchg.10).md">ReleaseHandle</a></td>
<td>Libere el identificador de esta instancia. (Invalida <a href="/dotnet/api/system.runtime.interopservices.safehandle.releasehandle#System_Runtime_InteropServices_SafeHandle_ReleaseHandle">SafeHandle.ReleaseHandle()</a>).</td>
</tr>
<tr class="even">
<td><img src="../images/dn292116.protmethod(exchg.10).gif" title="Método protegido" alt="Protected method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandle#System_Runtime_InteropServices_SafeHandle_SetHandle_System_IntPtr_">SetHandle</a></td>
<td>(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle).</a></td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.sethandleasinvalid#System_Runtime_InteropServices_SafeHandle_SetHandleAsInvalid">SetHandleAsInvalid</a></td>
<td>(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle).</a></td>
</tr>
<tr class="even">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn350935(v=exchg.10).md">Término</a></td>
<td>Finalice el JET_INSTANCE.</td>
</tr>
<tr class="odd">
<td><img src="../images/dn292146.pubmethod(exchg.10).gif" title="Método público" alt="Public method" /></td>
<td><a href="dn350960(v=exchg.10).md">ToString</a></td>
<td>Devuelve un <a href="/dotnet/api/system.string">objeto String</a> que representa la instancia <a href="dn350923(v=exchg.10).md">actual de</a>. (Invalida <a href="/dotnet/api/system.object.tostring#System_Object_ToString">Object.ToString()</a>).</td>
</tr>
</tbody>
</table>


Superior

## <a name="operators"></a>Operadores

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
<td><img src="../images/dn350944.puboperator(exchg.10).gif" title="Operador público" alt="Public operator" /><img src="../images/dn292146.static(exchg.10).gif" title="Miembro estático" alt="Static member" /></td>
<td><a href="dn350950(v=exchg.10).md">Implicit(Instance to JET_INSTANCE)</a></td>
<td>Proporcione la conversión implícita de un objeto Instance en una JET_INSTANCE estructura. Esto se hace para que una instancia se pueda usar en cualquier lugar en JET_INSTANCE se requiera una instancia de .</td>
</tr>
</tbody>
</table>


Superior

## <a name="fields"></a>Campos

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
<td><img src="../images/dn350944.protfield(exchg.10).gif" title="Campo protegido" alt="Protected field" /></td>
<td><a href="/dotnet/api/system.runtime.interopservices.safehandle.handle">handle</a></td>
<td>(Se hereda de <a href="/dotnet/api/system.runtime.interopservices.safehandle">SafeHandle).</a></td>
</tr>
</tbody>
</table>


Superior

## <a name="see-also"></a>Consulte también

#### <a name="reference"></a>Referencia

[Clase de instancia](./instance-class.md)

[Espacio de nombres Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)
